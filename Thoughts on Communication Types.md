# Thoughts on Communication Types

## The Communication Method

- Utilize *GRPC*, Quantum Core (`core`) as the server, Adapters as clients;
- Serialize with *Protobuf*;
- With a bidirectional streaming RPC defined as `rpc Process(stream Update) returns (stream Reply)`, that is, both sides send a sequence of messages using a read-write stream, which operate independently.

## `Update`

`Update` is the information sent to `core` by Adapter.

Types of `Update`:

- `Message` for new messages from somebody in some context;
- `Event` for non-message changes to the chat context;

### Concerns

- Should "A message get edited" be a `Message` or an `Event`?

## `Reply`

`Reply` is the information sent to Adapter by `core`.
# CQ Adapter Message Processing

```haskell
CQAdapter ::= (CQDll, QuantumCQClient)
CQDll :: CQMessage -> CQUpdate
QuantumCQClient :: CQUpdate -> Update

CQ :: Raw -> CQMessage
QuantumCore :: Update -> [Response]
```

CQ --Load Library--> CQ DLL --Socket--> Quantum CQ Client --GRPC--> Quantum Core

## CQUpdate Schema

```json
{
    "message": {
        "msgId": int32,
        "text": string,
        "qq": int64,
        "group": int64,
        "discuss": int64,
        "anonymous": string
    }
}
```


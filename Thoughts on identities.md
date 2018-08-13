# Thoughts on identities

IM specific info --IM Adapter--> adapter specific id --Core--> universe id

info of user1@im1 <--> <#struct: user1.im1> <--> <#default: universe id A>

info of user2@im1 <--> <#struct: user2.im1> <--> <#default: universe id B>

info of user1@im2 <--> <#struct: user1.im2> <--> <#default: universe id C>

by default, A, B and C should be different from each other

but there should be a way to "merge" them

```json
{
    uid: "some uid",
    identities: {
        "im1": "user1.im1",
        "im2": "user1.im2"
    }
}
```

...and then A == C
# HMAC

HMAC stands for "Hash-based Message Authentication Code".
It is very simple, and allows for a generic hash function.

1. If the key is too large, perform `key = hash(key)`
2. Calculate `inner = hash((key ^ ipad) || message)`
3. Calculate `digest = hash((key ^ opad) || digest)`

And that is it.

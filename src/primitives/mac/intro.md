# Message Authentication Codes

Message Authentication Codes are similar to hash functions.
They take arbitrary bytes and output a random but deterministic value,
however, MACs use a key to authenticate that the code was produced by a trusted party.

## Length Extensions

Naive MACs using a hash function are vulnerable to length extension attacks. For example,
let's say you have a construction like `HASH(key || message)`. Unfortunately, with SHA-256,
it is trivial to extend the message with arbitrary data and calculate a new forge signature.
[Example code](https://gist.github.com/conradludgate/8868d6ee8438fd1c60f3b22269f280d6)

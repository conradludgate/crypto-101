# Stream Cipher

Stream ciphers are an extremely versatile and secure form of cipher.

All stream ciphers can be represented by the following algorithm

```rust
// determine the block key from the state
let block_key = hash(state);
// progress the state forward
state.set_block_pos(state.get_block_pos() + 1);
// apply the key to the block by xor
block ^= block_key
```

Stream ciphers allow for encrypting data that can be streamed (hence the name).
This allows you to decrypt data without first having decrypted the block before.

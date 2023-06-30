# Stream Cipher

Stream ciphers are an extremely versatile and secure form of cipher.

All stream ciphers can be represented by the following algorithm

```rust
let state = init(key, iv);
for block in message {
    // determine the block key from the state
    let block_key = hash(state);
    // progress the state forward
    state = forward(state);
    // apply the key to the block by xor
    block ^= block_key
}
```

Stream ciphers allow for encrypting data that can be streamed (hence the name).
This allows you to decrypt data without first having decrypted the block before.

The enigma machine is a famous example of a stream cipher, however instead of XOR it used substitution.

## Theory

If the hash function is a strong pseudo random number generator, then the key stream
will be a high entropy random key. Since a one-time-pad (OTP) is provably secure with
a perfectly random key, then the stream cipher key stream will imitate that.

Insecurities lie in the deterministic factor of the key stream. Given a known
block plaintext, the block key is easily determined. If there's a way to reverse the
`let block_key = hash(state)` step, then an attacker can decrypt all following blocks.
This was the failure of the enigma machine. The state was directly related to the substitutions.
If the substitutions could be determined, then the state was trivially brute-forcable.


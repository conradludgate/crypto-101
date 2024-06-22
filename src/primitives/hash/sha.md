# SHA

Standing for "Secure Hash Algorithm", this is a family of cryptographic hash functions standardized by the NSA.

## SHA-1

Do not use SHA-1.

## SHA-2

SHA-2 is a good cryptographic hash function. Because it is such a commonly used function, it has several instructions
in x86 SSE and many modern ARMv8 chips. On an M2 Max, SHA-256 can hash about 2.4GB/s, and SHA-512 can hash about 1.5GB/s

There are many forms of SHA-2:
* `SHA-224` - 256 bit state/224 bit output
* `SHA-256` - 256 bit state/256 bit output
* `SHA-512/224` - 512 bit state/224 bit output
* `SHA-512/256` - 512 bit state/256 bit output
* `SHA-384` - 512 bit state/384 bit output
* `SHA-512` - 512 bit state/512 bit output

Some of them truncate the state, which reduces the effectiveness of certain length-extension attacks.

## SHA-3 (Keccak)

SHA-3 is a very different construction to SHA-2. It is considered to have far better security, especially in a post-quantum world. However,
it does not yet have common hardware support and thus is considerably slower.

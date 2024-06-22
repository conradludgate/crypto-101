# Cryptographic Hash Functions

A hash function takes an input set of bytes and outputs a 'digest' set of bytes.
The digest is always the same if the input is the same. For a cryptographic hash,
the reverse operation from digest to input is not possible.

## Randomness

The digest of a cryptographic hash function is pseudo-random.

## Uniqueness

A cryptographic hash digest is not guaranteed to be unique, but up to a certain
number of inputs, it can be assumed with a high probability. If we assume a 256-bit digest,
it would take 480 octillion different hash calculations to have even a 1 in 1 quintillion chance
of having a collision. For the breakdown of the mathematics, read about [Birthday attacks](https://en.wikipedia.org/wiki/Birthday_attack).

This uniqueness assumption relies on the cryptographic hash still being considered secure. MD5 and SHA1
both have practical collision attacks.

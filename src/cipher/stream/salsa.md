# Salsa/ChaCha

Salsa and ChaCha are two popular and secure stream ciphers.
They are quite configurable, allowing you to change the number of rounds the state goes through
to get the block key.

Standard configurations are

* Salsa8
* Salsa12
* Salsa20
* ChaCha8
* ChaCha12
* ChaCha20

Because the number defines how many rounds the state goes through to get the key, the performance is
inversely proportional to the number of rounds.Eg Salsa8 is 2.5x faster than Salsa20.

The implementations of Salsa and ChaCha are almost identical, so they have equivalent speeds
but the ChaCha variant is considered more secure as it's hash function is said to mix the internal
state more than the Salsa hash function.

There is also the "extended" XSalsa and XChaCha algorithms which allow you to use a larger initialisation value.

| Algorithm | Key Size | Initialisation Value Size |
| --- | --- | --- |
| Salsa | 256 bit | 64 bit |
| XSalsa | 256 bit | 192 bit |
| ChaCha | 256 bit | 96 bit |
| XChaCha | 256 bit | 192 bit |

Salsa20 is well known for being the cipher behind NaCl's secretbox.

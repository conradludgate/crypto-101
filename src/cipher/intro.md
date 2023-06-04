# Cipher

Ciphers represent symmetrical encryption. They take some input data (plaintext), a key, and an initialisation value
and they turn the data into a random looking blob (ciphertext) of the same length. The IV and random ciphertext can
be safely made public, and only the owner of the key is able to turn the ciphertext back into plaintext.

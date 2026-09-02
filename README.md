# Pure Python DES Encryption

A pure Python implementation of the **Data Encryption Standard (DES)** algorithm from scratch, without using third-party cryptographic libraries such as `PyCryptodome`.

## 📌 About the Project

This project implements the standard DES symmetric-key encryption algorithm using only Python's built-in features.

The implementation demonstrates the internal working of DES, including:

- Initial Permutation (IP)
- Final Permutation (FP)
- Key generation
- Permuted Choice 1 (PC-1)
- Permuted Choice 2 (PC-2)
- Left circular shifts
- Expansion permutation
- XOR operations
- S-Box substitution
- P permutation
- 16 Feistel rounds
- Encryption
- Decryption

## 🔐 What is DES?

**Data Encryption Standard (DES)** is a symmetric-key block cipher that operates on **64-bit blocks** of data using a **64-bit key**.

Although the key is 64 bits long, 8 bits are used as parity bits, leaving an effective key length of **56 bits**.

DES performs **16 rounds** of Feistel operations to transform plaintext into ciphertext.

## ⚙️ DES Algorithm

The overall encryption process is:

```text
64-bit Plaintext
       |
       v
Initial Permutation (IP)
       |
       v
    L0 + R0
       |
       v
  16 Feistel Rounds
       |
       v
   Swap Halves
       |
       v
Final Permutation (FP)
       |
       v
64-bit Ciphertext# security-DES
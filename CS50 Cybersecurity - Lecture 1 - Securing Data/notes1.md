# CS50 Cybersecurity - Lecture 1: Securing Data

## Table of Contents
- [CS50 Cybersecurity - Lecture 1: Securing Data](#cs50-cybersecurity---lecture-1-securing-data)
  - [📚 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [🔒 Storing Passwords Securely](#-storing-passwords-securely)
  - [🔐 Hashing Passwords](#-hashing-passwords)
  - [🧂 Salting Hashes](#-salting-hashes)
  - [🔑 Encryption Basics](#-encryption-basics)
  - [🔗 Public Key Cryptography](#-public-key-cryptography)
  - [✍️ Digital Signatures](#️-digital-signatures)
  - [🌐 End-to-End Encryption](#-end-to-end-encryption)
  - [🗑️ Secure Deletion of Data](#️-secure-deletion-of-data)
  - [🚀 Quantum Computing and Security](#-quantum-computing-and-security)
  - [📖 References](#-references)

---

## 🌟 Introduction
In this lecture, we explore the fundamentals of securing data, focusing on how passwords are stored, hashed, and protected. We also delve into encryption techniques, digital signatures, and the future of cybersecurity with quantum computing.

[🔝 Back to Top](#table-of-contents)

---

## 🔒 Storing Passwords Securely
When you create an account on a website or app, your username and password are stored on a server. In the simplest form, passwords can be stored in plain text, but this is highly insecure. If a hacker gains access to the database, they can easily steal all usernames and passwords.

**Why is this bad?**
- **Credential Stuffing**: Hackers can use stolen credentials to access other accounts if users reuse passwords.
- **Data Breaches**: Plain text passwords are vulnerable to leaks, exposing user data.

[🔝 Back to Top](#table-of-contents)

---

## 🔐 Hashing Passwords
To improve security, passwords are hashed before being stored. Hashing is a process that converts a password into a fixed-length string of characters, known as a hash value. This hash value is stored instead of the actual password.

**How does hashing work?**
- A hash function takes a password as input and produces a hash value.
- The same password will always produce the same hash value.
- Hash values are designed to be irreversible, meaning you cannot retrieve the original password from the hash.

**Example:**
- Password: `apple` → Hash: `..ekWXa83dhiA`
- Password: `banana` → Hash: `..ekWXa83dhiB`

**Why is hashing better?**
- Even if a hacker accesses the database, they only see hash values, not the actual passwords.

[🔝 Back to Top](#table-of-contents)

---

## 🧂 Salting Hashes
Hashing alone is not enough. If two users have the same password, their hash values will be identical, which can leak information. To prevent this, we use **salting**.

**What is salting?**
- A salt is a random value added to the password before hashing.
- Each user has a unique salt, so even if two users have the same password, their hash values will be different.

**Example:**
- Password: `cherry` + Salt: `50` → Hash: `50..ekWXa83dhiC`
- Password: `cherry` + Salt: `49` → Hash: `49..ekWXa83dhiD`

**Why is salting important?**
- It prevents attackers from identifying users with the same password.
- It adds an extra layer of security to the hashing process.

[🔝 Back to Top](#table-of-contents)

---

## 🔑 Encryption Basics
Encryption is the process of converting plain text into ciphertext to protect data. Unlike hashing, encryption is reversible, meaning you can decrypt the ciphertext back into the original message.

**Types of Encryption:**
1. **Symmetric Key Encryption**: The same key is used for both encryption and decryption.
2. **Asymmetric Key Encryption**: Different keys are used for encryption and decryption (public and private keys).

**Example: Caesar Cipher**
- A simple rotational cipher where each letter is shifted by a fixed number.
- Key: `1` → `A` becomes `B`, `B` becomes `C`, etc.

[🔝 Back to Top](#table-of-contents)

---

## 🔗 Public Key Cryptography
Public key cryptography uses a pair of keys: a public key and a private key. The public key is shared with everyone, while the private key is kept secret.

**How it works:**
- **Encryption**: Someone uses your public key to encrypt a message.
- **Decryption**: You use your private key to decrypt the message.

**Example Algorithms:**
- **RSA**: A widely used public key algorithm based on prime numbers.
- **Diffie-Hellman**: A key exchange algorithm that allows two parties to establish a shared secret.

[🔝 Back to Top](#table-of-contents)

---

## ✍️ Digital Signatures
Digital signatures are used to verify the authenticity of a message or document. They ensure that the message was sent by the claimed sender and has not been tampered with.

**How it works:**
1. The sender hashes the message.
2. The sender encrypts the hash with their private key, creating a digital signature.
3. The recipient decrypts the signature using the sender's public key and verifies the hash.

**Why is this important?**
- It provides proof of identity and integrity for digital communications.

[🔝 Back to Top](#table-of-contents)

---

## 🌐 End-to-End Encryption
End-to-end encryption ensures that data is encrypted from the sender to the recipient, with no intermediaries able to decrypt it.

**Examples:**
- **iMessage**: Messages are encrypted between Apple devices.
- **WhatsApp**: Messages are encrypted between users.

**Why is this important?**
- It protects your data from being accessed by third parties, including service providers.

[🔝 Back to Top](#table-of-contents)

---

## 🗑️ Secure Deletion of Data
When you delete a file, it is not immediately removed from your device. Instead, the operating system marks the space as available for reuse. To securely delete data, you must overwrite the existing data with random values.

**Methods:**
- **Overwriting**: Replace the data with zeros or random values.
- **Full-Disk Encryption**: Encrypt all data on the device, making it unreadable without the decryption key.

[🔝 Back to Top](#table-of-contents)

---

## 🚀 Quantum Computing and Security
Quantum computing has the potential to break current encryption methods by performing calculations exponentially faster than classical computers.

**Implications:**
- **Cryptography**: Current encryption algorithms may become obsolete.
- **Security**: New quantum-resistant algorithms will need to be developed.

[🔝 Back to Top](#table-of-contents)

---

## 📖 References
1. [CS50 Cybersecurity - Lecture 1 - Securing Data](https://www.youtube.com/watch?v=X3DVaMnl5n8&list=PLhQjrBD2T383Cqo5I1oRrbC1EKRAKGKUE&index=3)
2. [NIST Guidelines on Password Security](https://www.nist.gov)
3. [RSA Encryption](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
4. [Diffie-Hellman Key Exchange](https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange)
5. [End-to-End Encryption](https://en.wikipedia.org/wiki/End-to-end_encryption)

[🔝 Back to Top](#table-of-contents)

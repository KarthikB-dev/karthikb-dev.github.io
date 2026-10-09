---
layout: post
title: "Ciphers"
---


Cryptographic systems are either public key (asymmetric) or private key (symmetric). Symmetric encryption is done using a single key for encryption and decryption. DES is a historic (and obsolete!) symmetric key algorithm and AES is its modern and secure replacement. Asymmetric encryption entails having a public and private key. These keys are inverses of one another, meaning data encrypted with the private key can be returned to its original form with the public key and vice versa. RSA is one of the most widely used asymmetric or public key algorithms.

Cryptography is perhaps best known for encrypting messages. But how? And what else? Two other key uses are *data integrity* and *data origin authentication*. The former entails ensuring that data is not corrupted or maliciously modified, and the latter entails proving identity. But if the private key is private, when would it be used for encryption? One example is digital signatures. Here, a hash of a message is computed. A good hash has few collisions (multiple inputs having the same output) and features the avalance effect (small changes in the input completely change the output). Hashes are typically shorter than the original data so the original message cannot be produced from the hash. If the sender encrypts the hash with their private key, then it can be proven that it was them who sent it which allows for non-repudiation. Afterwards, the receiver computes the hash over the message themselves and ensures it matches the one that was provided.

What real world protocols use public and private key cryptography together? Cloudflare has an excellent [article](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/) on transport layer security (TLS), which is used for communication over a network.


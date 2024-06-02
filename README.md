# Text Encryption Using Cryptographic Algorithms

A simple Node.js module for encrypting and decrypting textual information using AES-256-CBC encryption.

## Overview

This project allows you to encrypt and decrypt textual information using strong AES-256-CBC encryption. Each encryption operation generates a unique Initialization Vector (IV), ensuring that the same plaintext encrypted multiple times will produce different ciphertexts.

## Installation

To use this encryption module in your Node.js project, install it via npm:

```sh
npm install text-encryption-crypto


Usage


const { encrypt, decrypt } = require('text-encryption-crypto');

// Set your encryption key (must be 256 bits, 32 characters)
process.env.ENCRYPTION_KEY = 'your-encryption-key';

// Encrypting a text
let encryptedText = encrypt('Hello, world!');
console.log('Encrypted:', encryptedText);

// Decrypting an encrypted text
let decryptedText = decrypt(encryptedText);
console.log('Decrypted:', decryptedText);

Security Note

Ensure your encryption key (ENCRYPTION_KEY) is kept secret and stored securely. It must be 32 characters long to be used with AES-256-CBC encryption.




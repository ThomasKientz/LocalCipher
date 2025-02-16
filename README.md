# CipherLink

A web-based encryption application that allows users to securely share messages through URLs.

## Overview

This app provides a simple way to share encrypted messages securely without requiring any backend infrastructure or user accounts. It's particularly useful for sharing sensitive information that shouldn't be sent via plain text in emails or messages.

## Key Features

### Core Functionality

- Users can encrypt messages with a password
- The encrypted message is embedded in a URL that can be shared
- Recipients can decrypt the message using the same password

### Security Implementation

- Uses modern cryptographic standards:
  - AES-GCM for encryption
  - PBKDF2 for key derivation (100,000 iterations)
  - Secure random salt and IV generation
  - SHA-256 hashing

### Technical Features

- Client-side encryption/decryption using the Web Crypto API
- No server required - everything happens in the browser
- The encrypted data is stored in the URL fragment (hash)
- Automatic clipboard copying of both encrypted URLs and decrypted messages

### User Interface

- Clean, responsive design that works on mobile and desktop
- Two main sections:
  - Encryption section: Text area for message input and password field
  - Decryption section: Password input for decrypting received messages

### Privacy Considerations

- No data is ever sent to a server
- Encrypted data is only shared via URL fragments
- Passwords are never stored or transmitted

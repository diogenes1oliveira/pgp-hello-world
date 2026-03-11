# pgp-hello-world

_PGP so easy even your mom can do it_

## Basics

### Common Operations

| Category            | Operation                                          | Probability of use                         |
| ------------------- | -------------------------------------------------- | ------------------------------------------ |
| **Creation**        | Generate new key pair (gpg --full-generate-key)    | Medium (few times in a lifetime)           |
|                     | Generate subkeys (gpg --edit-key > addkey)         | Low (advanced users)                       |
|                     | Create revocation certificate (gpg --gen-revoke)   | Low (only at creation or emergency)        |
| **Everyday use**    | Encrypt file/message (gpg -e)                      | Medium (depends on workflow)               |
|                     | Decrypt file/message (gpg -d)                      | Medium (depends on workflow)               |
|                     | Sign file/commit (gpg --sign / git commit -S)      | High (for those who use signatures)        |
|                     | Verify signature (gpg --verify)                    | High (for those who receive)               |
|                     | Export public key (gpg --export -a)                | High (sharing)                             |
|                     | Import public key (gpg --import)                   | High (receiving keys)                      |
| **Management**      | List keys (gpg --list-keys)                        | Very high (frequent query)                 |
|                     | List secret keys (gpg --list-secret-keys)          | Medium (less frequent)                     |
|                     | Edit key trust (gpg --edit-key > trust)            | Low (only for web of trust)                |
|                     | Refresh keys from a keyserver (gpg --refresh-keys) | Low (manual)                               |
|                     | Export to keyserver (gpg --send-keys)              | Low (only those who publish)               |
|                     | Fetch key from keyserver (gpg --recv-keys)         | Medium (alternative to importing)          |
| **Revocation**      | Revoke key (using certificate)                     | Very low (only in case of loss/compromise) |
|                     | Publish revocation to keyserver                    | Very low (rare)                            |
| **Web of Trust**    | Sign another user's key (gpg --sign-key)           | Low (keysigning events)                    |
|                     | Verify fingerprint (gpg --fingerprint)             | Medium (before signing/trusting)           |
| **Backup/Recovery** | Export private key (gpg --export-secret-keys -a)   | Low (only for backup)                      |
|                     | Import private key                                 | Low (recovery/migration)                   |

Reference:

- https://chat.deepseek.com/a/chat/s/074e9258-1537-4cfb-8dfb-ffd3caee4756
- https://chat.deepseek.com/a/chat/s/802fd9f9-5b09-42f0-94f3-ce0f9b5b82e1

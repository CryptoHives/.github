# .github
CryptoHives brings consistent, portable, and auditable cryptography to .NET — managed code first, OS quirks gone.

# CryptoHives 🐝🔐

**Cross-platform, fully managed cryptography for .NET**

CryptoHives is an open-source initiative to re-implement all .NET security and cryptographic functionality in **pure managed code**, ensuring consistent behavior across all operating systems.

---

## Why CryptoHives?

The current .NET ecosystem delegates many cryptographic operations (e.g., `X509Certificate2`, `RSA`) to the underlying OS libraries. This introduces limitations and inconsistencies:

- Some algorithms are unavailable on certain platforms. Code may only work on latest and greatest.  
- Behavior and edge-case handling can differ depending on the host system and the .NET version.
- As an example, EdDSA certificate signature support is still missing due to lack of support on Windows and macOS. 

By providing **managed implementations**, CryptoHives ensures:

- ✅ The same API and behavior, regardless of OS and .NET version 
- ✅ Support for algorithms missing from the native platform  
- ✅ Easier testing, portability, and security audits  

---

## Scope

- Full re-implementation of .NET cryptographic primitives and APIs  
- Drop-in replacements for platform-bound classes like `X509Certificate2`, `RSA`, elliptic curves and symmetric ciphers  
- Strict adherence to established standards and test vectors for correctness  
- Continued reliance on OS-level **only** where software implementation cannot guarantee sufficient security, e.g. entropy for secure random generators  

---

## Vision

A world where .NET developers can rely on **consistent, portable, and auditable cryptography**, independent of OS quirks—while still benefiting from the strongest available randomness sources.

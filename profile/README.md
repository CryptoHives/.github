## 🛡️ CryptoHives Open Source Initiative 🐝

An open, community-driven cryptography and performance library collection for the .NET ecosystem.

---

## 🐝 CryptoHives .NET Foundation

The **CryptoHives Open Source Initiative** is a collection of modern, high-assurance libraries for .NET, developed and maintained by **The Keepers of the CryptoHives**. 
Each package is designed for security, interoperability, and clarity — making it easy to build secure systems for high performance transformation pipelines and for cryptography workloads without sacrificing developer experience.

---

## Why CryptoHives Open Source Initiative?

The current .NET ecosystem delegates many cryptographic operations (e.g., `X509Certificate2`, `RSA`) to the underlying OS libraries. This introduces limitations and inconsistencies:

- Some algorithms are unavailable on certain platforms. Code may only work on latest and greatest.  
- Behavior and edge-case handling can differ depending on the host system and the .NET version.
- As an example, EdDSA certificate signature support is still missing due to lack of support on Windows and macOS. 

Providing **managed implementations** ensures:

- ✅ The same API and behavior, regardless of OS and .NET version 
- ✅ Support for algorithms missing from the native platform  
- ✅ Easier testing, portability, and security audits  

---

## Scope

- Full re-implementation of .NET cryptographic primitives and APIs  
- Drop-in replacements for platform-bound classes like `X509Certificate2`, `RSA`, elliptic curves and symmetric ciphers  
- Strict adherence to established standards and test vectors for correctness  
- Continued reliance on OS-level **only** where software implementation cannot guarantee sufficient security, e.g. hardware entropy for secure random generators.  
- Supporting libraries to optimize memory allocations and thread synchronization for high performance transformation pipelines and for cryptography workloads.

---

## Vision

A world where .NET developers can rely on **consistent, portable, and auditable cryptography**, independent of OS quirks.


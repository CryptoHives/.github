# CryptoHives Roadmap

The following roadmap prioritizes development phases for CryptoHives.  
Each phase delivers a usable milestone, ensuring adoption is possible even before all algorithms are complete.  

---

## Phase 1 — Core Foundations (MVP)
🎯 Goal: Replace most common .NET cryptographic APIs with managed equivalents.

- ✅ Symmetric
  - AES (CBC, GCM, CTR)
  - ChaCha20-Poly1305
- ✅ Hashing
  - SHA-2 family (SHA-256, SHA-384, SHA-512)
  - HMAC
  - HKDF
- ✅ Asymmetric
  - RSA (OAEP, PSS)
  - ECDSA P-256
  - Ed25519
- ✅ Certificates
  - `X509Certificate` basic parsing (PEM/DER)
- ✅ Random
  - OS entropy wrapper (`CryptoRandom`)

📦 Deliverable: `CryptoHives.Cryptography.Core`, `CryptoHives.Cryptography.Symmetric`, `CryptoHives.Cryptography.Asymmetric`, `CryptoHives.Cryptography.X509Certificates` (preview).  
💡 This phase enables developers to **drop-in replace most .NET crypto** (AES, RSA, certs).  

---

## Phase 2 — Interop & Protocols
🎯 Goal: Reach feature parity with .NET Core crypto for practical real-world use.

- Symmetric: AES-CCM, AES-XTS  
- Hashing: SHA-3, Blake2b  
- MACs: CMAC, Poly1305  
- Asymmetric: ECDSA P-384, P-521, X25519  
- Certificates: Chain validation, CRL, OCSP  
- Formats: PKCS#8, PKCS#12 import/export  
- Protocol Primitives: JWT, CMS (basic), TLS 1.3 cipher suite support  

📦 Deliverable: `CryptoHives.Cryptography.Formats`, `CryptoHives.Cryptography.Protocols` (early).  
💡 This phase ensures **compatibility for TLS, JWT, and PKI-heavy apps**.  

---

## Phase 3 — Advanced & Extended
🎯 Goal: Broader algorithm coverage and developer adoption.

- Symmetric: Legacy (3DES, Serpent, Camellia — optional)  
- Hashing: Blake3, SHAKE XOFs  
- Password Hashing: Argon2, scrypt  
- Asymmetric: Ed448, ECDSA optimizations  
- Protocols: SSH primitives, S/MIME  
- Hybrid key agreement: ECDH + Kyber  

📦 Deliverable: `CryptoHives.Cryptography.Hybrid`, `CryptoHives.Cryptography.KeyDerivation`.  
💡 This phase makes CryptoHives attractive for **modern security frameworks**.  

---

## Phase 4 — Post-Quantum Crypto (PQC)
🎯 Goal: Provide managed .NET support for NIST PQC algorithms.

- KEMs:
  - CRYSTALS-Kyber (ML-KEM)
  - HQC (backup KEM)  
- Signatures:
  - CRYSTALS-Dilithium (ML-DSA)
  - FALCON
  - SPHINCS+  
- Hybrid certificates (X.509 classical + PQC)  
- TLS 1.3 hybrid cipher suites  

📦 Deliverable: `CryptoHives.Cryptography.PQC`.  
💡 This phase enables **quantum-safe applications** and keeps CryptoHives future-proof.  

---

## Phase 5 — Security Hardening
🎯 Goal: Production-readiness with side-channel and compliance.

- Constant-time implementations  
- Memory zeroization  
- Wycheproof integration testing  
- NIST validation vectors  
- FIPS-compliant build mode  

📦 Deliverable: `CryptoHives.Cryptography.Utils`, `CryptoHives.TestVectors`.  
💡 This phase ensures **trustworthiness for production + audits**.  

---

## Phase 6 — Ecosystem & Tooling
🎯 Goal: Improve developer experience and community adoption.

- Migration guide from `System.Security.Cryptography`  
- Samples & docs for JWT, TLS, cert validation  
- Benchmarking suite  
- Plug-in model for future algorithms  
- Meta-package: `CryptoHives.Cryptography.All`  

📦 Deliverable: Docs, samples, benchmarks, `CryptoHives.Cryptography.All`.  
💡 This phase makes CryptoHives **developer-friendly and easy to adopt**.  

---

# 📌 Roadmap Summary
1. **Phase 1 (MVP)** → AES, SHA-2, RSA, Ed25519, X509 basic (drop-in replacement)  
2. **Phase 2** → Interop parity (TLS, JWT, PKCS)  
3. **Phase 3** → Extended algorithms (Argon2, Blake3, SSH, hybrid ECDH+Kyber)  
4. **Phase 4** → PQC (Kyber, Dilithium, Falcon, SPHINCS+)  
5. **Phase 5** → Security hardening (side-channel, Wycheproof, FIPS)  
6. **Phase 6** → Ecosystem (docs, samples, meta-package)  

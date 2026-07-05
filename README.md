## 🛡️ CryptoHives Open Source Initiative 🐝

An open, community-driven collection of cryptography and performance libraries.

---

## ✨ Overview

The **CryptoHives Open Source Initiative** is a collection of modern, high-assurance libraries for .NET, developed and maintained by **The Keepers of the CryptoHives**. 
Each package is designed for security, interoperability, and clarity — making it easy to build secure systems for high performance transformation pipelines and for cryptography workloads without sacrificing developer experience.

The **CryptoHives .NET Foundation** project serves as the first core building block for .NET libraries under the **CryptoHives Open Source Initiative** umbrella.

---

## 🧪 Development Policy

Development may use AI-assisted tooling; no guarantee of clean-room provenance is claimed.

### 🧱 Orthogonal by design
- Everything is built with free and open-source tooling — the .NET SDK, Visual Studio Community, VS Code, GitHub, Azure DevOps.
- Packages are meant to stand on their own; we try hard to avoid deep cross-dependencies between them.
- Dependencies on anything outside CryptoHives are kept minimal and limited to widely adopted, well-maintained libraries (e.g. `Microsoft.Extensions.*`).
- OS and hardware dependencies are avoided where possible, so behavior stays deterministic across platforms and runtimes — this matters especially for the crypto implementations.
- None of this is meant to replace or compete with the existing .NET class library. It's meant to complement it.

### ⚡ Built for performance
- Every package targets high throughput with no steady-state allocations, for both transformation pipelines and crypto workloads.
- Where it helps, algorithms use managed SIMD intrinsics with a scalar fallback for platforms that don't support them.
- Performance and memory usage are benchmarked against reference implementations, not just asserted.

### 🔐 Secure development policy
- All implementations are developed without reliance on operating system or native platform crypto providers
- Fully managed implementations of cryptographic algorithms, written from NIST/RFC/ISO specifications and verified against official test vectors
- No OS crypto dependency — deterministic results on every platform, in some cases even outperforming OS implementations
- Review process includes algorithm validation and benchmarking against other OS, .NET or native reference implementations

---

## 🔐 Security Policy

Security comes first here. If you find a vulnerability, please don't open a public issue — follow the process described on the [CryptoHives Security Page](https://github.com/CryptoHives/.github/blob/main/SECURITY.md) instead.

---

## 🔏 Code Signing

Packages aren't code-signed yet. The Keepers plan to add signing once there's enough demand (and funding) to justify it.

---

## 📝 No-Nonsense License Matters

This project is MIT-licensed because we believe in open collaboration. That said, we're aware MIT code gets sometimes copied, repackaged, and resold without credit — if you use this code, we'd appreciate it if you didn't do that:

- Give visible credit to the **CryptoHives Open Source Initiative** / **The Keepers of the CryptoHives** and link back to the source.
- Send improvements back upstream and report issues rather than silently forking.

None of that is legally required under MIT — it's just what makes open source worth doing.

---

## ⚖️ License

Every component is licensed under MIT. Source files carry the following SPDX header by default:

```csharp
// SPDX-FileCopyrightText: <year> The Keepers of the CryptoHives
// SPDX-License-Identifier: MIT
```

A few inherited components use their original MIT-style headers instead, kept as-is for provenance.

---

## 🐝 About The Keepers of the CryptoHives

The CryptoHives Open Source Initiative is maintained by **The Keepers of the CryptoHives**, a loose collective of developers working on open, verifiable, high-performance cryptography for .NET.

---

## 🧩 Contributing

Issues and pull requests are welcome. Please read the [Contributing Guide](https://github.com/CryptoHives/.github/blob/main/CONTRIBUTING.md) before sending a PR.

---

© 2026 The Keepers of the CryptoHives

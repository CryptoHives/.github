## 🛡️ CryptoHives Open Source Initiative 🐝

An open, community-driven cryptography and performance library collection for the .NET ecosystem.

---

## ✨ Overview

The **CryptoHives Open Source Initiative** is a collection of modern, high-assurance libraries for .NET, developed and maintained by **The Keepers of the CryptoHives**. 
Each package is designed for security, interoperability, and clarity — making it easy to build secure systems for high performance transformation pipelines and for cryptography workloads without sacrificing developer experience.

The **CryptoHives .NET Foundation** project serves as the first core building block for .NET libraries under the **CryptoHives Open Source Initiative** umbrella.

---

## 🧪 Development Policy

Development may use AI-assisted tooling; no guarantee of clean-room provenance is claimed.

### 🔐 Managed Code Cryptography
- All implementations are developed without reliance on operating system or native platform crypto providers
- Fully managed implementations of cryptographic algorithms, written from NIST/RFC/ISO specifications and verified against official test vectors
- No OS crypto dependency — deterministic results on every platform, in some cases even outperforming OS implementations
- Review process includes algorithm validation and benchmarking against other OS, .NET or native reference implementations

### ⚡ High-Performance Primitives
- CryptoHives provides a growing set of utilities designed to optimize high performance transformation pipelines and cryptography workloads
- All utilities and cryptographic algorithms are benchmarked against available OS and third party libraries with a focus on memory allocations and performance

### 🧱 Orthogonal Design
- All development is done on free and open-source tools, e.g. .NET SDK, Visual Studio Community Edition, Visual Studio Code, GitHub, Azure DevOps, etc.
- Each package is designed to be orthogonal and composable with other CryptoHives packages to avoid deep cross dependencies
- Dependencies on other packages are kept to a minimum and shall only include widely adopted, well-maintained libraries, e.g. the Microsoft.Extensions
- OS and hardware dependencies are avoided wherever possible to ensure deterministic behavior across all platforms and runtimes, specifically for security implementations
- There is no intention to replace or shadow existing .NET class libraries; instead, CryptoHives packages are designed to complement and extend existing functionality

---

## 🔐 Security Policy

Security is our top priority.

If you discover a vulnerability, **please do not open a public issue.**  
Instead, please follow the guidelines on the [CryptoHives Open Source Initiative Security Page](https://github.com/CryptoHives/.github/blob/main/SECURITY.md).

---

## 📝 No-Nonsense Matters

This project is released under the MIT License because open collaboration matters.  
However, the Keepers are well aware that MIT-licensed code often gets copied, repackaged, or commercialized without giving credit.  

If you use this code, please do so responsibly:
- Give visible credit to the **CryptoHives Open Source Initiative** or **The Keepers of the CryptoHives** and refer to the original source.
- Contribute improvements back and report issues.

Open source thrives on respect, not just permissive licenses.

---

## ⚖️ License

Each component of the CryptoHives Open Source Initiative is licensed under a SPDX-compatible license.  
By default, packages use the following license tags:

```csharp
// SPDX-FileCopyrightText: <year> The Keepers of the CryptoHives
// SPDX-License-Identifier: MIT
```

Some inherited components may use alternative MIT license headers, according to their origin and specific requirements those headers are retained.

---

## 🐝 About The Keepers of the CryptoHives

The **CryptoHives Open Source Initiative** project is maintained by **The Keepers of the CryptoHives** —  
a collective of developers dedicated to advancing open, verifiable, and high-performance cryptography in .NET.

---

## 🧩 Contributing

Contributions, issue reports, and pull requests are welcome!

Please see the [Contributing Guide](https://github.com/CryptoHives/.github/blob/main/CONTRIBUTING.md) before submitting code.

---

**CryptoHives Open Source Initiative — Secure. Deterministic. Performant.**

© 2026 The Keepers of the CryptoHives. All rights reserved.

## 🛡️ CryptoHives Open Source Initiative 🐝

An open, community-driven collection of cryptography and performance libraries for the .NET ecosystem.

.NET is a solid platform for building secure, high-performance applications across almost any target, but two gaps keep showing up: high-performance patterns rarely get packaged as simple, drop-in libraries, and cryptography still leans heavily on whatever the underlying OS happens to provide, with all the inconsistency in features and performance that brings. 

CryptoHives exist to close both gaps, one package at a time.

The **CryptoHives Open Source Initiative** is maintained by **The Keepers of the CryptoHives** and is currently addressing three areas:

- **Threading** — async synchronization primitives built for low/no allocation and high throughput, using `ValueTask`-based waiters backed by pooled resources
- **Memory** — buffer management on top of `ArrayPool<T>` and the modern .NET memory APIs, meant to keep GC pressure out of transformation pipelines and crypto workloads
- **Cryptography** — OS-independent implementations for a wide range of cryptographic algorithms, usable as drop-in replacement for `System.Security.Cryptography`

---

## 🐝 Projects

### [CryptoHives .NET Foundation](https://github.com/CryptoHives/Foundation)

The first core building block of the initiative: pooled async primitives, ArrayPool-based buffers, and a fully managed cryptography library — including the complete NIST post-quantum set (ML-KEM, ML-DSA, SLH-DSA) on every target from .NET Framework 4.6.2 to .NET 10.

#### 📦 NuGet Packages

| Package | Description | NuGet | Documentation |
|----------|--------------|--------|---------------|
| `Memory` | Pooled buffers and streams | [![NuGet](https://img.shields.io/nuget/v/CryptoHives.Foundation.Memory.svg)](https://www.nuget.org/packages/CryptoHives.Foundation.Memory) | [Docs](https://cryptohives.github.io/Foundation/packages/memory/index.html) |
| `Threading` | Pooled async synchronization | [![NuGet](https://img.shields.io/nuget/v/CryptoHives.Foundation.Threading.svg)](https://www.nuget.org/packages/CryptoHives.Foundation.Threading) | [Docs](https://cryptohives.github.io/Foundation/packages/threading/index.html) |
| `Threading.Analyzers` | Analyzer for pooled async synchronization | [![NuGet](https://img.shields.io/nuget/v/CryptoHives.Foundation.Threading.Analyzers.svg)](https://www.nuget.org/packages/CryptoHives.Foundation.Threading.Analyzers) | [Docs](https://cryptohives.github.io/Foundation/packages/threading.analyzers/index.html) |
| `Security.Cryptography` | Cryptographic algorithms | [![NuGet](https://img.shields.io/nuget/v/CryptoHives.Foundation.Security.Cryptography.svg)](https://www.nuget.org/packages/CryptoHives.Foundation.Security.Cryptography) | [Docs](https://cryptohives.github.io/Foundation/packages/security/cryptography/index.html) |

All packages are published under the `CryptoHives.Foundation` prefix and namespace — see [CryptoHives on NuGet](https://www.nuget.org/packages?q=CryptoHives) for the full list.

#### 🩺 Health

[![Azure DevOps](https://dev.azure.com/cryptohives/Foundation/_apis/build/status%2FCryptoHives.Foundation?branchName=main)](https://dev.azure.com/cryptohives/Foundation/_build/latest?definitionId=6&branchName=main)
[![Tests](https://github.com/CryptoHives/Foundation/actions/workflows/buildandtest.yml/badge.svg)](https://github.com/CryptoHives/Foundation/actions/workflows/buildandtest.yml)
[![codecov](https://codecov.io/github/CryptoHives/Foundation/graph/badge.svg?token=02RZ43EVOB)](https://codecov.io/github/CryptoHives/Foundation)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FCryptoHives%2FFoundation.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FCryptoHives%2FFoundation?ref=badge_shield)

---

## 📚 Documentation

- 📖 **[Full Documentation](https://cryptohives.github.io/Foundation/)** — guides, API reference, examples
- 🚀 [Getting Started Guide](https://cryptohives.github.io/Foundation/getting-started.html)
- 📦 [Package Documentation](https://cryptohives.github.io/Foundation/packages/index.html) — what each package gives you, with links to its guides
- 📚 [API Reference](https://cryptohives.github.io/Foundation/api/index.html) — every public namespace, generated from the source
- ⏱️ **Live benchmark dashboards** — [Cryptography](https://cryptohives.github.io/Foundation/packages/security/cryptography/benchmarks.html) · [Threading](https://cryptohives.github.io/Foundation/packages/threading/benchmarks.html)

---

## 🧬 Development Policy

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

### 🛡️ Secure development policy
- Implementations are written directly from public specifications (NIST, RFC, ISO) rather than ported from other codebases.
- Every algorithm is checked against official test vectors from its specification.
- Reviews include validation against independent reference implementations.
- Public APIs and anything touching the network are treated as hostile-input surfaces by default.
- Defaults favor a minimal attack surface: explicit configuration, strict input validation, bounded resource use.
- Dependencies are kept minimal and vetted; reproducible, signed releases are on the roadmap.
- Fuzzing is planned; static analysis and defensive error handling are already in place to limit misuse and information leaks.

### 🤖 AI Usage in This Project
AI coding assistants (such as Claude and GitHub Copilot) are used in this project as productivity tools — for drafting boilerplate, tests, and documentation, and for reviewing code. 
Every AI-assisted contribution is reviewed, understood, and validated by a human maintainer before being merged; no code is accepted that the maintainers cannot fully explain and stand behind. 
Given the security-sensitive nature of this library, all cryptographic logic is verified against the relevant specifications and test vectors regardless of how it was authored. 
Contributors are welcome to use AI tools under the same principle: you are responsible for the correctness, licensing, and quality of what you submit, and purely machine-generated PRs without human understanding will be rejected.

---

## 🚨 Security Policy

Security comes first here. If you find a vulnerability, please don't open a public issue — report it privately through [GitHub's private vulnerability reporting](https://github.com/CryptoHives/Foundation/security/advisories/new). The [CryptoHives Security Page](https://github.com/CryptoHives/.github/blob/main/SECURITY.md) has the details.

---

## 🔏 NuGet Package Code Signing

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

---

## 🐝 About The Keepers of the CryptoHives

The CryptoHives Open Source Initiative is maintained by **The Keepers of the CryptoHives**, a loose collective of developers working on open, verifiable, high-performance cryptography for .NET.

---

## 🤝 Contributing

Issues, questions and pull requests are all welcome — small ones just as much as big ones. Issues labelled [`good first issue`](https://github.com/CryptoHives/Foundation/labels/good%20first%20issue) or [`help wanted`](https://github.com/CryptoHives/Foundation/labels/help%20wanted) are a good place to start. Have a look at the [Contributing Guide](https://github.com/CryptoHives/.github/blob/main/CONTRIBUTING.md) and our short [Code of Conduct](https://github.com/CryptoHives/.github/blob/main/CODE_OF_CONDUCT.md).

---

© 2026 The Keepers of the CryptoHives

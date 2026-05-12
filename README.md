# Artem — VoroN5k

**Full Stack Developer · Cryptography Enthusiast · Privacy Advocate**

> *"Privacy is not a luxury, nor a gift from the state. It is a fundamental human right."*

---

## What I Build

I design and ship systems where **trust is mathematical, not institutional** — software that protects people even when the infrastructure it runs on cannot be trusted.

### 🦇 Vesper Messenger
An open-source, fully E2E-encrypted messenger I built from scratch. Not a proof-of-concept — a production system with real cryptographic depth.

- **Signal Double Ratchet** (X25519 + AES-256-GCM) for direct messages — per-message forward secrecy
- **Signal Sender Key** protocol for group chats — Ed25519-signed broadcast chains
- **X3DH** key exchange — asynchronous session establishment without a trusted third party
- **Per-device envelopes** — each physical browser gets its own X25519 identity; messages fan out per device
- **Argon2id PIN vault** — private keys encrypted at rest, never transmitted; replaced PBKDF2 for GPU resistance
- **VSP-1** — custom device sync protocol over WebRTC DataChannel, OTP-secured, HMAC-manifest verified
- **Rust → WASM** — the entire Signal stack runs in a dedicated Web Worker, isolated from the DOM

All crypto implemented in Rust (`x25519-dalek`, `ed25519-dalek`, `aes-gcm`, `argon2`) with `ZeroizeOnDrop` on every secret type.

→ [github.com/VoroN5k/messenger-web-app](https://github.com/VoroN5k/messenger-web-app)

---

## Current Research

| Topic | Status |
|---|---|
| **OPAQUE** (asymmetric PAKE) — eliminate password exposure at the server | 🔬 Exploring |
| **Shamir's Secret Sharing** — threshold-based key recovery without central custodians | 🔬 Exploring |
| **Key transparency / safety numbers** — verifiable public key pinning for Vesper | 📋 Planned |

---

## Tech Stack

| Layer | Technologies |
|---|---|
| **Languages** | Rust, TypeScript, JavaScript (ES6+) |
| **Backend** | NestJS, Node.js, Prisma, PostgreSQL, Redis, Socket.io |
| **Frontend** | Next.js 15, React 19, TailwindCSS, Zustand |
| **Cryptography** | Signal Protocol, X3DH, Double Ratchet, Argon2id, AES-256-GCM, Ed25519, X25519 |
| **Runtime** | WebAssembly (wasm-bindgen, wasm-pack), Web Workers, WebRTC |
| **Infrastructure** | Fly.io, Vercel, Docker, Supabase |

---

## Code Integrity

All commits are cryptographically signed. If a commit on my account is not verified, it didn't come from me.

- **PGP Fingerprint:** `E378 6523 64F6 9745 6F80 5D98 203B FD38 6BF1 0FD5`
- **Public key:** [keys.openpgp.org](https://keys.openpgp.org/search?q=E378652364F697456F805D98203BFD386BF10FD5)
- **Commit status:** Verified ✅

---

## Stats

![GitHub Stats](https://github-readme-stats-eight-theta.vercel.app/api?username=VoroN5k&show_icons=true&theme=radical&hide_border=true)
![Top Languages](https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=VoroN5k&layout=compact&theme=radical&hide_border=true)

---

*Building the decentralised web, one encrypted byte at a time.*
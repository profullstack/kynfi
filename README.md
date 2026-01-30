# Kynfi

**Secure file & photo sync across all your devices.**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Web](https://img.shields.io/badge/web-kynfi.com-green.svg)](https://kynfi.com)

---

## 🚀 Features

- **📁 File Sync** - Seamlessly sync files across desktop, mobile, and web
- **📷 Photo Backup** - Automatic photo backup from your phone
- **🔐 End-to-End Encryption** - Your files are encrypted before they leave your device
- **📜 Version History** - Restore previous versions of any file
- **🗑️ Trash & Recovery** - Recover accidentally deleted files
- **💳 Flexible Payments** - Pay with card (Stripe) or crypto (CoinPayPortal)

---

## 📦 Apps

| Platform | Description | Status |
|----------|-------------|--------|
| **Web** | Dashboard at [kynfi.com](https://kynfi.com) | 🚧 In Development |
| **Desktop** | Windows, macOS, Linux (Electron) | 🚧 In Development |
| **Mobile** | iOS & Android (Expo) | 🚧 In Development |
| **CLI** | Command-line tool for power users | 🚧 In Development |

---

## 🏗️ Architecture

This is a **monorepo** powered by [pnpm](https://pnpm.io/) and [Turborepo](https://turbo.build/).

```
kynfi.com/
├── apps/
│   ├── web/          # Next.js web application
│   ├── desktop/      # Electron desktop app
│   ├── mobile/       # Expo mobile app
│   └── cli/          # CLI tool
│
├── packages/
│   ├── @kynfi/types/      # Shared TypeScript types
│   ├── @kynfi/utils/      # Shared utilities
│   ├── @kynfi/sync-core/  # Core sync engine
│   ├── @kynfi/crypto/     # End-to-end encryption
│   ├── @kynfi/ui/         # Shared UI components
│   ├── @kynfi/supabase/   # Supabase client & hooks
│   ├── @kynfi/payments/   # Stripe + CoinPayPortal
│   └── @kynfi/config/     # Shared configs
│
└── plans/            # Architecture documentation
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React, Next.js, Expo, Electron |
| **State** | Zustand |
| **Backend** | Supabase (Auth, Database, Storage, Realtime) |
| **Payments** | Stripe, CoinPayPortal |
| **Encryption** | XChaCha20-Poly1305, Argon2id |
| **Build** | Turborepo, pnpm, TypeScript |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) >= 18
- [pnpm](https://pnpm.io/) >= 8

### Installation

```bash
# Clone the repository
git clone https://github.com/kynfi/kynfi.com.git
cd kynfi.com

# Install dependencies
pnpm install

# Set up environment variables
cp .env.example .env.local
# Edit .env.local with your Supabase and Stripe keys

# Start development
pnpm dev
```

### Development Commands

```bash
# Start all apps in development mode
pnpm dev

# Build all apps
pnpm build

# Run linting
pnpm lint

# Run tests
pnpm test

# Clean build artifacts
pnpm clean
```

### Running Individual Apps

```bash
# Web app only
pnpm dev --filter=web

# Desktop app only
pnpm dev --filter=desktop

# Mobile app only
pnpm dev --filter=mobile

# CLI only
pnpm dev --filter=cli
```

---

## 📖 Documentation

| Document | Description |
|----------|-------------|
| [Architecture](./plans/monorepo-architecture.md) | Monorepo structure, apps, packages |
| [Sync & Conflicts](./plans/three-way-merge.md) | 3-way merge for text files |
| [Version History](./plans/version-history.md) | File versioning and trash |
| [Payments](./plans/payments.md) | Stripe and crypto payments |
| [Encryption](./plans/encryption.md) | End-to-end encryption |

---

## 💳 Pricing

| Plan | Price | Storage | Version History |
|------|-------|---------|-----------------|
| **Free** | $0 | 5 GB | 7 days |
| **Pro** | $9.99/mo | 100 GB | 30 days |
| **Business** | $19.99/mo | 1 TB | 90 days |
| **Enterprise** | Custom | Unlimited | 365 days |

---

## 🔐 Security

Kynfi uses **end-to-end encryption** to protect your files:

- **XChaCha20-Poly1305** for file encryption
- **Argon2id** for password-based key derivation
- **X25519** for secure multi-device key exchange
- Files are encrypted **before** leaving your device
- Kynfi servers **cannot** read your files

[Learn more about our encryption →](./plans/encryption.md)

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🔗 Links

- **Website**: [kynfi.com](https://kynfi.com)
- **Documentation**: [docs.kynfi.com](https://docs.kynfi.com)
- **Status**: [status.kynfi.com](https://status.kynfi.com)
- **Support**: support@kynfi.com

---

<p align="center">
  Made with ❤️ by the Kynfi team
</p>

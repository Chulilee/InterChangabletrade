# LuminaryTrade

> **A TypeScript monorepo that connects blockchain integrations (Stellar + Soroban) with AI services for trading, credit scoring, fraud detection, and risk automation.**

---

## 📖 What is LuminaryTrade?

**LuminaryTrade** is a production-ready platform for building AI-driven financial services on the Stellar blockchain. It bridges decentralized finance (DeFi) with artificial intelligence to enable trustless, intelligent financial services.

### What It Does

LuminaryTrade combines three core pillars:

1. **Stellar Blockchain Integration**
   - Direct connection to Stellar Horizon API for account data, transaction history, and on-chain state
   - Soroban smart contracts for immutable, verifiable scoring and fraud detection results
   - Native support for Stellar assets and payments

2. **AI-Powered Analysis**
   - **Credit Scoring**: Calculate creditworthiness from on-chain and off-chain signals
   - **Fraud Detection**: Real-time machine learning analysis of transactions
   - **Risk Signals**: Predictive analytics for portfolio and counterparty assessment
   - Pluggable AI providers (OpenAI, custom models, etc.)

3. **Enterprise-Grade Backend & Frontend**
   - REST API and WebSocket support for real-time updates
   - React dashboards for monitoring and analytics
   - Background workers for batch processing and automation
   - Full JWT authentication and role-based access control

### What It's For

LuminaryTrade enables teams to rapidly build:

- **🏦 Lending Platforms**: Automated credit scoring and underwriting with blockchain verification
- **🚨 Fraud Prevention Systems**: Real-time transaction monitoring and anomaly detection
- **📊 Risk Management**: Portfolio analysis and risk signal generation
- **🤖 Algorithmic Trading**: Trading bots with AI-enhanced decision making
- **✅ Compliance Systems**: Trustless verification and immutable audit trails
- **💼 Financial Services**: Any DeFi application needing AI-powered decisions backed by blockchain

### Who Should Use It

- **DeFi Platforms** building lending, trading, or derivatives protocols
- **Blockchain Teams** integrating Stellar with AI decision systems
- **FinTech Innovators** combining centralized and decentralized finance
- **Enterprise Blockchain** deploying regulated financial services on-chain
- **Teams** that need to ship AI + blockchain features in weeks, not months

---

## 🎯 Core Value Propositions

| Feature | Benefit |
|---------|---------|
| **Blockchain-Verified Decisions** | AI decisions recorded immutably on-chain for compliance and audit trails |
| **Fully Typed TypeScript** | Catch errors at compile time, not production; full IDE support |
| **Production Ready** | Database pooling, caching, rate limiting, error handling all built-in |
| **Composable Architecture** | Use individual packages (SDKs, services) or the full platform |
| **Quick Start** | Working examples and CLI tools get you productive in hours |
| **Monorepo Layout** | Backend, frontend, contracts, docs all in one place with shared types |

---

## ✨ Key Features

### 🔗 Blockchain Integration
- **Stellar Horizon Client**: Type-safe wrapper around Stellar Horizon REST API
- **Soroban Contracts**: Smart contract helpers for on-chain verification and state management
- **Account Management**: Track balances, transactions, and account history
- **Asset Operations**: Seamless asset issuance, trading, and payment workflows

### 🧠 AI & Machine Learning
- **Credit Scoring**: Calculate creditworthiness based on on-chain and off-chain signals
- **Fraud Detection**: Machine learning models for transaction anomaly detection
- **Risk Signals**: Predictive risk assessment for portfolio and counterparty analysis
- **Pluggable Providers**: Support for multiple AI providers (OpenAI, custom models, etc.)

### ⚙️ TypeScript-First Development
- **Strongly Typed SDKs**: Full TypeScript support with comprehensive type definitions
- **Node & Browser Support**: SDKs work in both server and client environments
- **Monorepo Structure**: Shared types and utilities across all packages
- **Build Tooling**: Modern build pipelines with hot reload and production optimization

### 🛠 Developer Experience
- **CLI Tools**: Command-line utilities for contract deployment, account management, and testing
- **Example Applications**: Reference implementations for common use cases
- **Comprehensive Docs**: Architecture guides, API references, and integration tutorials
- **DevOps Scripts**: Automation for building, testing, and deploying to testnet/mainnet

### 📊 Analytics & Monitoring
- **Dashboard UI**: Real-time visualization of accounts, scores, and risk signals
- **Audit Logs**: Immutable transaction history on-chain and in database
- **Metrics**: Performance monitoring and analytics for scoring and fraud detection
- **Alerts**: Configurable alerts for high-risk events and anomalies

---

## 📁 Project Structure

```text
luminarytrade/
├── backend/                  # Backend services and APIs
│   ├── src/                  # API source code (controllers, services, models)
│   ├── tests/                # Unit & integration tests
│   └── README.md
├── frontend/                 # Frontend applications and UI components
│   ├── apps/                 # Multiple apps (dashboard, wallet, etc.)
│   ├── components/           # Shared React components
│   └── README.md
├── contracts/                # Soroban smart contracts and build artifacts
│   ├── credit-score/         # Credit scoring contract(s)
│   ├── fraud-detect/         # Fraud detection contract(s)
│   └── common-utils/         # Shared contract utilities & tests
├── examples/                 # Example integrations & reference apps
│   ├── credit-scoring-app/
│   ├── wallet-chatbot/
│   └── fraud-detection-service/
├── packages/                 # Shared TypeScript packages / SDKs
│   ├── core/                 # Core SDK (connectors, types, utilities)
│   └── cli/                  # CLI tools and scripts
├── docs/                     # Documentation (guides, API reference)
├── scripts/                  # Build, deploy, and automation scripts
├── tests/                    # End-to-end and system tests
├── .github/                  # CI workflows, issue templates, PR templates
└── README.md                 # This file
```

---

## 🚀 Quick Start

### Prerequisites

- **Node.js**: v18 or higher (LTS recommended)
- **pnpm**: v8+ (recommended) or npm/yarn
- **Docker**: For local PostgreSQL, Redis, and contract testing (recommended)
- **AI Provider API Key**: When using hosted AI features (e.g., OpenAI)

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/GameChangable/luminarytrade.git
cd luminarytrade
```

2. **Install dependencies**

```bash
pnpm install
```

3. **Set up environment variables**

```bash
# Copy example environment file
cp .env.example .env

# Edit .env with your configuration
# - Database URL (PostgreSQL)
# - Redis URL
# - Stellar network (testnet/public)
# - AI provider API keys
```

4. **Start local services** (using Docker)

```bash
docker-compose up -d
```

This starts:
- PostgreSQL database
- Redis cache
- (Optional) Soroban local testnet

---

## 💻 Development

### Backend Development

```bash
cd backend

# Install dependencies
pnpm install

# Start development server (with hot reload)
pnpm dev

# Run tests
pnpm test

# Run tests in watch mode
pnpm test:watch

# Build for production
pnpm build
```

**Default API Endpoints**:
- Health: `GET /api/health`
- Credit Score: `GET /api/accounts/:accountId/credit-score`
- Fraud Detection: `POST /api/transactions/analyze`

### Frontend Development

```bash
cd frontend

# Install dependencies
pnpm install

# Start development server
pnpm start

# Run tests
pnpm test

# Build for production
pnpm build
```

**Access the app**:
- Dashboard: http://localhost:3000
- Admin Panel: http://localhost:3001

### Smart Contract Development

```bash
cd contracts/credit-score

# Install dependencies
pnpm install

# Build contract
pnpm build

# Run tests
pnpm test

# Deploy to testnet
pnpm deploy:testnet
```

### Using the Core SDK

```typescript
import { StellarConnector, AIService, CreditScorer } from '@luminarytrade/core';

// Initialize Stellar connection
const stellar = new StellarConnector({
  network: 'testnet',
  horizonUrl: 'https://horizon-testnet.stellar.org',
});

// Initialize AI service
const ai = new AIService({
  provider: 'openai',
  apiKey: process.env.AI_API_KEY,
});

// Initialize credit scorer
const scorer = new CreditScorer(stellar, ai);

// Get an account and calculate credit score
async function main() {
  const account = await stellar.getAccount('GXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX');
  const score = await scorer.calculateScore(account);
  
  console.log('Account:', account.id);
  console.log('Credit Score:', score.rating);
  console.log('Risk Level:', score.riskLevel);
}

main().catch(console.error);
```

---

## 🏗 Architecture

### System Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    Frontend Applications                      │
│              (React Dashboard, Wallet, Admin)                │
└────────────────────────┬────────────────────────────────────┘
                         │ HTTPS / WebSocket
┌────────────────────────▼────────────────────────────────────┐
│                   Backend API Layer                           │
│  (REST API, WebSocket, Authentication, Rate Limiting)        │
└────────────────────────┬────────────────────────────────────┘
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
   ┌─────────┐     ┌──────────┐    ┌──────────┐
   │Database │     │  Redis   │    │  Workers │
   │(PostgreSQL)   │ (Cache)  │    │(Background)
   └─────────┘     └──────────┘    └──────────┘
        │
        └────────────────┬────────────────┐
                         │                │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
   ┌──────────┐    ┌──────────┐    ┌──────────┐
   │ Stellar  │    │ AI/ML    │    │ Soroban  │
   │ Horizon  │    │ Services │    │ Contracts│
   │   API    │    │(OpenAI)  │    │(On-Chain)│
   └──────────┘    └──────────┘    └──────────┘
```

### Key Components

**Backend Services**:
- **API Server**: Express/Fastify REST API handling client requests
- **Authentication**: JWT-based auth with refresh token rotation
- **Account Service**: Track and manage user accounts on Stellar
- **Scoring Service**: Calculate credit scores using AI models
- **Fraud Detection**: Real-time transaction analysis
- **Worker Pool**: Background jobs for long-running operations

**Frontend Applications**:
- **Dashboard**: Analytics and account monitoring
- **Wallet**: Stellar wallet operations and payments
- **Admin Panel**: System management and configuration

**Blockchain Layer**:
- **Stellar Connection**: Horizon API integration for account and transaction data
- **Soroban Contracts**: On-chain scoring and verification logic
- **Smart Contract Helpers**: TypeScript utilities for contract interaction

**AI Integration**:
- **Credit Scoring Model**: Trained model for creditworthiness assessment
- **Fraud Detection Model**: Anomaly detection for suspicious transactions
- **Risk Signals**: Predictive analytics for portfolio management
- **Provider Abstraction**: Support for multiple AI providers

---

## ⚙️ Configuration & Environment Variables

### Backend (.env)

```env
# Server
PORT=3000
NODE_ENV=development

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/luminary
DATABASE_POOL_SIZE=20

# Redis (caching and sessions)
REDIS_URL=redis://localhost:6379/0

# Stellar
STELLAR_NETWORK=testnet
STELLAR_HORIZON_URL=https://horizon-testnet.stellar.org
STELLAR_SERVER_SIGNING_KEY=SXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# AI Services
AI_PROVIDER=openai
AI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
AI_MODEL=gpt-4

# JWT Authentication
JWT_SECRET=your-secret-key-here
JWT_EXPIRY=1h
JWT_REFRESH_EXPIRY=7d

# Logging
LOG_LEVEL=info
LOG_FORMAT=json

# CORS
CORS_ORIGIN=http://localhost:3000,http://localhost:3001

# Email (for notifications)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
```

### Frontend (.env.local)

```env
REACT_APP_API_URL=http://localhost:3000/api
REACT_APP_STELLAR_NETWORK=testnet
REACT_APP_WS_URL=ws://localhost:3000
REACT_APP_SENTRY_DSN=https://your-sentry-dsn@sentry.io/1234567
```

---

## 📚 API Reference

### Authentication

All API requests require a Bearer token:

```bash
curl -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  http://localhost:3000/api/accounts
```

### Key Endpoints

**Accounts**:
- `GET /api/accounts/:id` - Get account details
- `GET /api/accounts/:id/credit-score` - Get credit score
- `GET /api/accounts/:id/transactions` - Get account transactions

**Scoring**:
- `POST /api/scoring/calculate` - Calculate credit score
- `POST /api/scoring/explain` - Explain score factors

**Fraud Detection**:
- `POST /api/fraud-detect/analyze` - Analyze transaction for fraud
- `GET /api/fraud-detect/alerts` - Get fraud alerts

**Admin**:
- `GET /api/admin/health` - System health check
- `GET /api/admin/metrics` - Performance metrics

See `docs/api-reference.md` for complete endpoint documentation.

---

## 🔗 Smart Contracts

### Credit Scoring Contract

On-chain contract for immutable credit score verification:

```rust
pub fn calculate_credit_score(
    account: Address,
    balance: i128,
    transaction_count: u32,
) -> i32
```

**Features**:
- Deterministic scoring based on on-chain data
- Immutable score history
- Audit trail for compliance

### Fraud Detection Contract

Verify fraud detection results on-chain:

```rust
pub fn verify_fraud_score(
    transaction_id: String,
    fraud_score: i32,
    timestamp: u64,
) -> bool
```

See `contracts/` directory and `docs/smart-contracts.md` for details.

---

## 📝 Examples

### Example 1: Basic Credit Scoring

See `examples/credit-scoring-app/` for a complete working example.

### Example 2: Fraud Detection Service

See `examples/fraud-detection-service/` for a standalone fraud detection implementation.

### Example 3: Trading Bot with AI Signals

See `examples/trading-bot/` for an algorithmic trading example.

### Example 4: Wallet Chatbot

See `examples/wallet-chatbot/` for a conversational wallet interface.

---

## 🤝 Contributing

We welcome contributions from the community! Please follow these guidelines:

### Getting Started

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add feature description"`
4. Push to your fork: `git push origin feature/your-feature-name`
5. Open a Pull Request

### Development Standards

- Write tests for new features (aim for >80% coverage)
- Follow the TypeScript style guide in `CONTRIBUTING.md`
- Update documentation for API changes
- Ensure all tests pass before submitting PR

### Code Review Process

1. At least one maintainer review required
2. All CI checks must pass
3. Address feedback and push updates
4. Merge after approval

See `CONTRIBUTING.md` for detailed guidelines.

---

## 📖 Documentation

- **`docs/architecture.md`** - System design and component relationships
- **`docs/authentication.md`** - JWT auth flow and security best practices
- **`docs/api-reference.md`** - Complete API endpoint documentation
- **`docs/smart-contracts.md`** - Contract architecture and deployment
- **`docs/deployment.md`** - Production deployment guide
- **`docs/integration-guide.md`** - How to integrate LuminaryTrade
- **`docs/ai-providers.md`** - AI provider configuration
- **`docs/troubleshooting.md`** - Common issues and solutions

---

## 🆘 Support & Community

- **Issues**: Open an issue for bug reports or feature requests
- **Discussions**: Use GitHub Discussions for questions and ideas
- **Email**: contact@luminarytrade.dev

---

## 👥 Maintainers

- Maintained by the **GameChangable** team
- For urgent issues, tag maintainers in PRs or open an issue with the `urgent` label

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Stellar Development Foundation** for the Stellar blockchain and Horizon API
- **Soroban** team for smart contract platform
- **OpenAI** and other AI providers for ML capabilities
- **Community contributors** who have helped improve this project

---

## 🔮 Roadmap

- [ ] Multi-chain support (Ethereum, Polygon)
- [ ] Advanced portfolio analytics
- [ ] Real-time trading execution
- [ ] Enhanced mobile app
- [ ] GraphQL API
- [ ] Kafka integration for event streaming
- [ ] Enhanced AI model fine-tuning

---

**Last Updated**: June 5, 2026

For the latest updates, visit [GitHub](https://github.com/GameChangable/luminarytrade).

# AgentPay

### Machine-to-Machine Payment Protocol on Stellar

AgentPay is a decentralized **machine-to-machine (M2M) payment protocol** built on the Stellar network that enables autonomous agents, APIs, software services, and IoT devices to pay each other instantly using micro-payments.

The protocol provides **usage-based billing infrastructure** for the emerging AI and automation economy — enabling services to charge per API call, per compute request, or per data query.

AgentPay acts as **"Stripe for AI agents"**, allowing software systems to transact autonomously without human intervention.

---

## 1. Problem

The rapid growth of **AI agents, APIs, and autonomous software services** is creating a new type of economy where machines consume services from other machines.

Examples:

| Scenario | Description |
|--------|-------------|
| AI Agent → API | Agent pays for data or compute |
| Autonomous Vehicle → Charging Station | Pays for electricity |
| Trading Bot → Analytics API | Pays per market query |
| IoT Sensor → Data Network | Pays for storage or bandwidth |

### Current Challenges

| Problem | Impact |
|-------|--------|
| No micro-billing infrastructure | APIs cannot charge per request |
| Payment rails too expensive | Fees exceed transaction value |
| Manual billing systems | Not suitable for autonomous agents |
| No global protocol | Fragmented ecosystem |
| Lack of trustless settlement | Requires centralized platforms |

Most payment systems are **not designed for high-frequency micro-transactions** between machines.

---

## 2. Solution

AgentPay introduces a **machine-to-machine payment protocol** built on the Stellar blockchain.

Services can publish pricing models, and agents can pay automatically based on usage.

### Core Idea

Machines interact economically without human involvement.

### Workflow

1. Service provider publishes API pricing
2. AI agents deposit stablecoins
3. Agent consumes service
4. Usage is tracked
5. Smart contracts settle payment automatically

Example:

**AI Agent → Weather API**  
Cost: $0.002 per request

If the agent makes **1000 requests**, the system automatically settles:

**Total Payment = $2**

---

## 3. Key Features

- **Pay-Per-Request Billing** — Services can charge per API request, compute usage, bandwidth, dataset access
- **Autonomous Payments** — AI agents can pay services without human approval
- **Global Micro-Transactions** — Payments in fractions of a cent using stablecoins
- **Smart Contract Settlement** — Usage and payments handled by Soroban smart contracts
- **API Marketplace** — Developers can list APIs and earn revenue from autonomous agents

---

## 4. Why Stellar

| Feature | Benefit |
|------|------|
| Ultra-low fees | Enables micro-payments |
| Fast settlement | ~5 seconds |
| Stablecoin ecosystem | USDC / other tokens |
| Asset issuance | Easy token creation |
| Global accessibility | Borderless payments |

---

## 5. Repository Structure

| Repository | Description |
|------------|-------------|
| [agentpay-contracts](./agentpay-contracts) | Soroban smart contracts (escrow, settlement) |
| [agentpay-backend](./agentpay-backend) | API gateway, metering, billing (Express) |
| [agentpay-frontend](./agentpay-frontend) | Dashboard and wallet integration (Next.js) |

---

## 6. System Architecture

- **Agent** → **AgentPay Gateway** → **Usage Metering** → **Soroban Contract** → **Stellar Network**
- Gateway forwards requests to API providers and records usage; contracts settle micro-payments.

---

## 7. Payment Flow

1. Agent sends API request to Gateway
2. Gateway forwards to API Provider
3. Gateway records usage
4. Contract updates usage and settles micro-payment on Stellar
5. Provider receives stablecoin transfer

---

## 8. Tech Stack

- **Frontend:** Next.js, React, TailwindCSS, Stellar wallet integration
- **Backend:** Node.js, Express, gRPC microservices, REST APIs
- **Blockchain:** Stellar, Soroban Smart Contracts, Horizon API
- **Infrastructure:** Docker, PostgreSQL, Redis, Kafka

---

## 9. License

MIT

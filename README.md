# t-Market: Ecosystem Marketplace & Commercial Engine

![Status](https://img.shields.io/badge/Status-Alpha-orange) ![License](https://img.shields.io/badge/License-MIT-green) ![Tech](https://img.shields.io/badge/Tech-Next.js%20%7C%20Stripe%20%7C%20Firebase-blue)

**t-Market** is the commercial backbone of the **T-Ecosystem**, designed to be the central hub for acquiring, managing, and billing software modules. It transforms the ecosystem from a set of tools into a scalable SaaS platform, handling everything from user subscriptions to enterprise licensing.

## 🚀 Capabilities & Features

### 🛒 Digital Marketplace

- **Module Discovery**: Browse a catalog of T-Ecosystem modules (ENV-I, UPH, Weave, Renderci).
- **Rich Product Pages**: Detailed feature breakdowns, version history, and pricing tiers for each module.
- **Add-on System**: Purchase capability expansions (e.g., "Extra Storage", "Advanced Analytics Pack").

### 💳 Secure Payments & Billing

- **Stripe Integration**: Robust payment processing for credit cards and subscription billing.
- **Subscription Management**: Self-serve upgrades/downgrades with automated proration logic.
- **Invoicing**: Auto-generated compliant PDF invoices for every transaction.
- **Usage-Based Billing**: Support for tiered pricing based on seats, storage, or API calls.

### 👤 User & Organization Management

- **Unified Account**: Single Sign-On (SSO) identity management across the entire ecosystem.
- **Billing Profiles**: Manage multiple payment methods and billing addresses.
- **License Management**: Assign purchased seats to specific team members.

### 🤖 Intelligent Features

- **Smart Recommendations**: Suggests modules based on user usage patterns (e.g., "You use Inventory often, try the Advanced Warehouse Map").
- **Cross-Sell & Up-Sell**: Targeted promotions and bundle offers.

## 🛠️ Technology Architecture

- **Framework**: [Next.js 15](https://nextjs.org/) (App Router)
- **Payments**: **Stripe API** (Webhooks & Checkout Sessions)
- **Database**: **Firebase Firestore** (User data & Order history)
- **Styling**: Tailwind CSS
- **State**: Zustand

## 📂 Project Structure

```bash
app/
├── store/           # Marketplace catalog & product pages
├── cart/            # Shopping cart logic
├── checkout/        # Stripe Checkout integration
├── account/         # User dashboard & billing settings
├── api/             # Stripe Webhooks & Server-side logic
└── login/           # Authentication flows
```

## 🏁 Getting Started

### Prerequisites

- Node.js (v18+)
- pnpm
- Stripe Account (Test Mode)

### Installation

1.  **Clone the repository**

    ```bash
    git clone https://github.com/alazndy/t-market.git
    cd t-market
    ```

2.  **Install Dependencies**

    ```bash
    pnpm install
    ```

3.  **Environment Setup**
    Create `.env.local` with Stripe and Firebase keys:

    ```env
    NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=...
    STRIPE_SECRET_KEY=...
    NEXT_PUBLIC_FIREBASE_API_KEY=...
    ```

4.  **Run Development Server**

    ```bash
    pnpm dev
    ```

    Open [http://localhost:3002](http://localhost:3002) to view the marketplace.

---

Part of the **T-Ecosystem**.

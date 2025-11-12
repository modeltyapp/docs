# Modelty Documentation

**Investor-facing documentation** for Modelty's wallet-first creator platform.

This repository contains comprehensive documentation for:

- **Company Information** — MDLY Holding, roadmap, security, architecture
- **Product Suite** — Oruon (wallet), Ops (AI), RemoveMyContent (vault)
- **AI Strategy** — Manager AI and Integrity AI approaches
- **Strategy & Moat** — Competitive advantages and lock-in analysis
- **Investor Resources** — Metrics access and contact information
- **Resources** — FAQ and glossary

## 🌐 Live Documentation

Visit the live documentation at: **[docs.modelty.app](https://docs.modelty.app)** *(configure your actual domain)*

## 📁 Documentation Structure

```
docs/
├── index.mdx                    # Homepage with overview
├── company/                     # Company information
│   ├── mdly-holding.mdx        # Corporate structure
│   ├── roadmap.mdx             # Timeline and roadmap
│   ├── security.mdx            # Security & compliance
│   ├── architecture.mdx        # Technical architecture
│   └── gtm.mdx                 # Go-to-market strategy
├── products/                    # Product documentation
│   ├── overview.mdx            # Product suite overview
│   ├── oruon.mdx               # Oruon wallet
│   ├── ops.mdx                 # Ops (Sasha) AI
│   └── removemycontent.mdx     # Vault & protection
├── ai-strategy/                 # AI approach
│   ├── manager-ai.mdx          # Manager AI (Ops)
│   └── integrity-ai.mdx        # Integrity AI (Vault)
├── strategy/                    # Strategic analysis
│   └── moat.mdx                # Competitive moat
├── investors/                   # Investor resources
│   └── overview.mdx            # Metrics & contact
├── resources/                   # Additional resources
│   ├── faq.mdx                 # Frequently asked questions
│   └── glossary.mdx            # Terms and definitions
└── assets/                      # Images and media
    └── README.md               # Asset specifications
```

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Install our GitHub app from your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app) to propagate changes from your repo to your deployment. Changes are deployed to production automatically after pushing to the default branch.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)

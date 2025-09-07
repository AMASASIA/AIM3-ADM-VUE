
# Vue × WalletConnect × ETH Transfer — AI Gate Chat (Mock)

This project mirrors your mockups:
- Chat-centered UX
- WalletConnect login
- DID message signing
- ETH transfer
- AI Advocacy gate (local rule-based; replace with your API)

## Run
```bash
npm i
cp .env.example .env
# put VITE_WALLETCONNECT_PROJECT_ID
npm run dev
```

## Notes
- For production, move AI moderation to a server (Next.js API or any backend) and call OpenAI or your Custom AI.
- `TransferCard` uses `eth_sendTransaction` via WalletConnect provider.
- `SignMessage` uses `personal_sign` for DID-like proof.

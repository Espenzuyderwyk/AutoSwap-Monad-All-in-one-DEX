# Daily Swap Monad (Rubic, Hedgemony, Taya.fi, Bubble.fi) 

<img width="1728" height="972" alt="image" src="https://github.com/user-attachments/assets/fa247fd3-65bb-498b-96d5-f8726a7b7f86" />

An automated bot for performing token swaps on **Monad Testnet** using multiple platforms:
- **Rubic** (MON ↔ WMON)
- **TayaSwap** (MON ↔ USDC/WETH)
- **Hedgemony** (MON ↔ HEDGE)
- **BubbleFi** (PEPE ↔ MLDK ↔ MYK swaps)

This bot runs 24/7 with randomized daily transactions, random delays, and built-in retry logic to avoid RPC limits.

## ✨ Features
- **Multi-platform automated swaps** (4 types)
- **Randomized daily transaction count** (57–98)
- **Randomized delay between swaps** (3–8 minutes)
- **Automatic retries** when hitting RPC limits
- **API status updates** for Rubic & Hedgemony

### * Don't forget to claim faucet and approve manually (just one time) on: 
- https://testnet.rubic.exchange
- https://app.taya.fi/swap
- https://app.bubblefi.xyz/
- https://app.sherpa.trade/lander

## Installation

Clone the repository
```bash
git clone https://github.com/Espenzuyderwyk/AutoSwap-Monad-All-in-one-DEX.git
cd AutoSwap-Monad-All-in-one-DEX
```

Install packages
```bash
npm install
```

Edit and input Private Key, Bearer, and Cookie:
```bash
nano .env
```

Run the script
```bash
node index.js
```

### * If this bot doesn't work, you can swap manually first.

# How to get Cookie?
1. Go to dex Monad Ecosystem (Rubic and Bubblefi)
2. Login your wallet
3. Approve manually (just one time)
4. Click F12 on your keyboard
5. Click Network
6. Search status_info
7. Scroll and you can see your Cookie

<img width="1154" height="732" alt="Cookie" src="https://github.com/user-attachments/assets/a9b842c6-0c1f-4a11-b5b6-af522a4fa973" />

# How to get Bearer?
1. Go to dex Monad Ecosystem ( Hedgemony )
2. Login your wallet
3. Click F12 on your keyboard
4. Click Application
5. Click Local Storage
6. On Key u can see hedgemony_auth and Value is your Bearer
7. Copy all bearer and paste on .env

<img width="1152" height="648" alt="Bearer" src="https://github.com/user-attachments/assets/89a4affd-9bba-4dec-a477-28fe7e1b74d1" />

## ⚙️ Environment Variables

See **.env.example** for the complete format:

| Variable           | Description                                       |
| ------------------ | ------------------------------------------------- |
| `RPC_URL`          | Monad Testnet RPC URL                             |
| `PRIVATE_KEY`      | Your wallet private key (hex format without `0x`) |
| `WMON_ADDRESS`     | WMON contract address                             |
| `ROUTER_ADDRESS`   | Router contract address for WMON                  |
| `RUBIC_API_URL`    | Rubic API endpoint                                |
| `RUBIC_COOKIE`     | Rubic authentication cookie                       |
| `HEDGEMONY_BEARER` | Bearer token for Hedgemony API                    |
| `HEDGE_ADDRESS`    | HEDGE token contract address                      |
| `BUBBLEFI_COOKIE`  | BubbleFi authentication cookie                    |

## Troubleshooting

- Ensure your private keys are in Base58 format
- Verify your wallets
- Check approving and swapping
- Monitor console for error messages

## License

MIT License - See LICENSE file for details

## Disclaimer

This bot is for educational purposes only. Use at your own risk. The maintainers are not responsible for any lost funds or account issues.

## 🖼️ NFT Marketplace — Built with Next.js, TypeScript & Solidity

This project is a **full-stack NFT Marketplace** built using modern Web3 technologies.
It allows users to **mint, list, and purchase NFTs** on a local or test blockchain network.

> 🎓 Full tutorial available:
> [NFT Marketplace in React, TypeScript & Solidity - Full Guide](https://academy.eincode.com/courses/nft-marketplace-in-react-js-next-typescript-full-guide)

---

## 🚀 Tech Stack

* **Frontend:** [Next.js](https://nextjs.org/), [React](https://reactjs.org/), [TypeScript](https://www.typescriptlang.org/)
* **Smart Contracts:** [Solidity](https://soliditylang.org/), [Truffle](https://trufflesuite.com/)
* **Blockchain Network:** [Ganache](https://trufflesuite.com/ganache/)
* **File Storage & Metadata:** [Pinata](https://app.pinata.cloud/) (IPFS-based)
* **Environment Management:** `.env.development`

---

## ⚙️ Getting Started

### 1️⃣ Install Dependencies

Run the following command in the root directory:

```bash
npm install
```

---

### 2️⃣ Configure Environment Variables

Create a file named `.env.development` in the root directory and add:

```bash
NEXT_PUBLIC_NETWORK_ID=5777
NEXT_PUBLIC_TARGET_CHAIN_ID=1337
NEXT_PUBLIC_PINATA_DOMAIN=https://gateway.pinata.cloud

SECRET_COOKIE_PASSWORD={your_32+_character_password}

PINATA_API_KEY={your_pinata_api_key}
PINATA_SECRET_API_KEY={your_pinata_secret_api_key}
```

> 💡 Make sure your Pinata API keys have permissions for
> `pinFileToIPFS` and `pinJSONToIPFS`.

---

### 3️⃣ Deploy the Smart Contract

The main contract is `NftMarket.sol` (located in the `contracts` folder).
To deploy it locally:

```bash
truffle migrate
```

Make sure **Ganache** is running and linked correctly:

* Open Ganache → click **Add Project**
* Select your project folder
* Ensure `truffle-config.js` points to your Ganache network

If you’re **not deploying to Ropsten**, remove the `keys.json` import and comment out the Ropsten configuration in `truffle-config.js`.

---

### 4️⃣ Run the Application

After successful migration, start the development server:

```bash
npm run dev
```

Your app will be available at:

```
http://localhost:3000
```

---

## ✅ Summary

| Step | Action               | Description                            |
| ---- | -------------------- | -------------------------------------- |
| 1    | Install Dependencies | `npm install`                          |
| 2    | Set Up Environment   | Create `.env.development`              |
| 3    | Deploy Contracts     | `truffle migrate` with Ganache running |
| 4    | Run App              | `npm run dev`                          |

---

## 🧩 Features

* Mint and list NFTs
* View and buy NFTs
* Pin image and metadata to IPFS via Pinata
* Local blockchain testing with Ganache

---

## 🛠️ Troubleshooting

* **Contract not found:** Re-run `truffle migrate --reset`
* **API errors:** Double-check your Pinata API keys
* **Ganache issues:** Ensure Ganache network matches your Truffle config

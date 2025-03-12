# **🔥 Avax Gods - Online Multiplayer Web3 NFT Card Game**  
![Gameplay](https://i.ibb.co/4P2C08x/image.png)  

Welcome to **Avax Gods**, an immersive **Web3-powered multiplayer NFT card game** built on the **Avalanche blockchain**! 🃏⚡ This game lets players battle in a **decentralized** environment, trade unique NFT cards, and experience the power of smart contracts in gaming.  

## **🚀 Ready to build and play? Let’s dive in!**  

---

## **🛠️ Setting Up the Web3 Environment**  

To deploy and interact with the smart contract, follow these steps carefully:  

### **📌 Step 1: Navigate to the Web3 Directory**  
Move into the Web3 folder where the smart contract and blockchain logic are stored:  
```sh
cd web3
```

### **📌 Step 2: Initialize Hardhat**  
Set up **Hardhat**, the Ethereum development environment, by running:  
```sh
npx hardhat
```
- Select **TypeScript** when prompted (`y → typescript → enter → enter`).  
- This sets up a project with TypeScript support for better security and development experience.  

### **📌 Step 3: Install Dependencies**  
You'll need several dependencies to work with smart contracts and blockchain interactions:  

🔹 **OpenZeppelin Contracts** for secure smart contract development:  
```sh
npm install @openzeppelin/contracts dotenv @nomiclabs/hardhat-ethers
```
🔹 **Hardhat Development Toolbox** to ease contract deployment and testing:  
```sh
npm install --save-dev "hardhat@^2.12.0" "@nomicfoundation/hardhat-toolbox@^2.0.0"
```

---

## **🔗 Connecting Your Wallet to Avalanche Testnet**  

### **📌 Step 4: Install Core Wallet Extension**  
For seamless interaction with the **Avalanche blockchain**, install [Core Wallet](https://chrome.google.com/webstore/detail/core/agoakfejjabomempkjlepdflaleeobhb), a **Metamask alternative** designed for Avalanche dApps.  

### **📌 Step 5: Enable Testnet Mode**  
After installing Core Wallet:  
1. Open the **Core extension**.  
2. Click the **hamburger menu (☰) in the top left**.  
3. Navigate to **Advanced Settings**.  
4. Turn on **Testnet Mode** to interact with the Fuji test network.  

### **📌 Step 6: Fund Your Wallet with AVAX**  
You need testnet AVAX tokens to deploy and interact with the smart contract.  
1. Visit the [AVAX Faucet](https://faucet.avax.network/).  
2. Enter your wallet address and request **free testnet AVAX**.  

---

## **🔑 Setting Up Private Keys Securely**  

### **📌 Step 7: Create a `.env` File**  
To securely store your private key, create a **.env** file inside the `web3` directory:  
```sh
touch .env
```
Inside `.env`, add your **PRIVATE_KEY**:  
```sh
PRIVATE_KEY=your_private_key_here
```

### **📌 Step 8: Extract Your Private Key from Core Wallet**  
1. Open **Core Wallet** → Click ☰ (menu).  
2. Go to **Security & Privacy** → Click **Show Recovery Phrase**.  
3. Enter your password and copy the **mnemonic phrase**.  
4. Go to [wallet.avax.network](https://wallet.avax.network/) → Click **Access Wallet**.  
5. Select **Mnemonic Key Phrase** → Paste your recovery phrase.  
6. In the sidebar, go to **Manage Keys** → **View C-Chain Private Key**.  
7. Copy your private key and paste it into the `.env` file.  

🔴 **WARNING**: Never share your **private key**—treat it like your password!  

---

## **📜 Deploying the Smart Contract**  

### **📌 Step 9: Copy the Required Files**  
- **`hardhat.config.ts`** → Configuration file for Hardhat.  
- **`deploy.ts`** → Deployment script.  
- **`AvaxGods.sol`** → The actual smart contract.  

### **📌 Step 10: Compile the Smart Contract**  
Ensure there are no syntax errors before deployment:  
```sh
npx hardhat compile
```
If everything is correct, you’ll see a success message confirming compilation.  

### **📌 Step 11: Deploy to Avalanche Fuji Testnet**  
Run the following command to deploy your smart contract:  
```sh
npx hardhat run scripts/deploy.ts --network fuji
```
After deployment, copy the **contract address** displayed in the terminal.  

---

## **📂 Integrating the Smart Contract with the Frontend**  

### **📌 Step 12: Move the Compiled Contract JSON File**  
Once the contract is deployed, move the compiled **AVAXGods.json** file into the frontend:  
```sh
mv artifacts/contracts/AVAXGods.json frontend/contract
```

### **📌 Step 13: Link the Contract Address in the Frontend**  
Open `/contract/index.js` in the frontend and paste the **contract address** you copied earlier.  

---

## **🎮 You’re Ready to Play!**  

🚀 Now your **Avax Gods** NFT card game is fully deployed on the **Avalanche Fuji Testnet**! Players can **battle, trade NFTs, and experience decentralized gaming** like never before.  

💡 Want to customize the game? Modify the **Solidity smart contract** and **React frontend** to add new features!  

💬 If you run into any issues, feel free to ask for help or contribute to the project!  

**Happy coding, and may the best player win!** 🃏🔥  

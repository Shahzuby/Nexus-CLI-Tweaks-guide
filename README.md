Nexus Prover Node — Optimized Setup Guide (ZeekeAlpha)

This guide helps you set up a fully optimized Nexus Prover Node using the official GitHub source code. It is 100% beginner-friendly and uses your existing Node ID from the Nexus Dashboard.


---

✅ Features:

Built from source (not precompiled)

Optimized config (numWorkers, proofTimeout)


---

🧰 VPS Requirements:

Ubuntu 22.04+

4 vCPU / 8 GB RAM minimum (16GB preferred)

20 GB disk space


---

🔧 Step-by-Step Installation

1. Update and Install Dependencies

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install git curl build-essential nano screen -y
```

2. Install Node.js v18 using NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
```

3. Install Rust
```bash
curl https://sh.rustup.rs -sSf | sh -s -- -y
source ~/.cargo/env
```

4. Install Yarn
```bash
npm install -g yarn
```

5. Clone Nexus Repo and Build From Source
```bash
cd ~
git clone https://github.com/nexus-xyz/nexus-cli.git
cd nexus-cli
yarn install
yarn build
```

6. Create Config with Your Node ID
```bash
mkdir ~/.nexus
nano ~/.nexus/config.json
```

Paste the following (replace with your actual Node ID and wallet):
```bash
{
  "nodeId": "YOUR_NODE_ID",
  "wallet": "YOUR_WALLET_ADDRESS",
  "numWorkers": 4,
  "proofTimeout": 600
}
```
Save with Ctrl + X, then Y, then Enter.

7. Run Node in Screen Session
```bash
screen -S nexus
cd ~/nexus-cli
node dist/index.js start
```

To detach screen (let node run in background):

Ctrl + A → then D

8. Reconnect to Screen Anytime
```bash
screen -r nexus
```

---

✅ You're All Set!

Your Nexus prover node is now:

Fully optimized

Built from source

Using your real Node ID

Running 24/7 in a screen session


---

🔗 Connect with Me

Twitter: https://x.com/ZeekeAlpha

Telegram: https://t.me/andhiiTGkamaii

YouTube: https://youtube.com/@zeekeyt


Stay tuned for more nodes, airdrops, and testnet guides 🚀


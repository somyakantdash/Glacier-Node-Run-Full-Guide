# Glacier-Node-Run-Full-Guide

## Node System Requirements

https://docs.glacier.io/getting-started/glacier-nodes/run-testnet-nodes/using-docker

## Need Some Requirements for PC Users

1. Install Docker - https://www.docker.com/products/docker-desktop/

2. Install WSL - https://learn.microsoft.com/en-us/windows/wsl/install#install-wsl-command

   🍀For VPS (Additional Only for VPS Users to Download Docker)
```
sudo apt update -y
```
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```
```
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt update -y
```
```
apt-cache policy docker-ce
```
```
sudo apt install docker-ce -y
```
```
sudo usermod -aG docker ${USER}
su - ${USER}
groups
```

## Preparation of Private Key and Gas Fees

1. Create a New wallet

2. Add opBNB RPC: https://chainlist.org/chain/5611

3. Get Some Testnet BNB Faucet: https://docs.bnbchain.org/bnb-smart-chain/developers/faucet/

4. Bridge ur Testnet BNB faucet TO Testnet opBNB Faucet: https://opbnb-testnet-bridge.bnbchain.org/deposit

## Own Your Node License

Currently, we will automatically mint the Node License NFT for you on the OpBNB Testnet the first time the verifier node goes online and is registered on the smart contract, eliminating the need for you to request it manually. Please note that the minting process may take several minutes.

## Run A Node
```
docker run -d -e PRIVATE_KEY=Private_Key --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.3
```

Note: Must Replace "Private_Key" with your actual Wallet Private Key

## Check ur Logs
```
docker logs -f glacier-verifier
```

## Check ur Status

https://testnet.nodes.glacier.io/status

## Check ur NFT

https://testnet.opbnbscan.com/

## 🔶For Next Day Run This Command

#1 Open docker 1st 

#2 Now Open WSL and Put this Command 
```
docker run -d -e PRIVATE_KEY=Private_Key --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.3
```
Note: Must Replace "Private_Key" with your actual Wallet Private Key
```
docker logs -f glacier-verifier
```

# Glacier Points - Season III

🍀Go: https://tinyurl.com/bdemp4ru

👉Do galxe task & collects points as much as possible

from web3 import Web3

# Connect to an Ethereum node (this is a free public RPC - you can replace with your own)
infura_url = 'https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID'  # replace with your own
web3 = Web3(Web3.HTTPProvider(infura_url))

if not web3.isConnected():
    print("❌ Failed to connect to Ethereum network")
    exit()

wallet_address = input("Enter Ethereum wallet address: ")

try:
    balance_wei = web3.eth.get_balance(wallet_address)
    balance_eth = web3.fromWei(balance_wei, 'ether')
    print(f"✅ Wallet Balance: {balance_eth} ETH")
except Exception as e:
    print(f"Error: {e}")
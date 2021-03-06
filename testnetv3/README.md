# TestnetV3 

## Usage
Copy the config details of Main chain and Matic chain into a separate file named `<main/matic>-addresses.json`. Import into the file you'd like to use the addresses in. 

```javascript
const mainAddresses = require('./main-addresses.json')
const maticAddresses = require('./matic-addresses.json')
```
Then use it in your Matic SDK config or anywhere else as: 

```javascript
let matic = new Matic ({
  depositManager: mainAddresses[Contracts].DepositManager
  ...
  ...
})
```
## Addresses
### Main

    "Main": {
      "NetworkName": "Ropsten testnet",
      "ChainId": 3,
      "RPC": "https://ropsten.infura.io/v3/70645f042c3a409599c60f96f6dd9fbc",
      "SyncerAPI": "https://testnetv3-syncer.api.matic.network/api/v1",
      "WatcherAPI": "https://testnetv3-watcher.api.matic.network/api/v1",
      "DaggerEndpoint": "https://ropsten.dagger.matic.network",
      "Explorer": "https://ropsten.etherscan.io",
      "Contracts": {
        "Registry": "0x56B082d0a590A7ce5d170402D6f7f88B58F71988",
        "RootChain": "0x82a72315E16cE224f28E1F1fB97856d3bF83f010",
        "DepositManager": "0x4b068Ac93b3b71DB13Fce4c4510Eb70D3022576A",
        "DepositManagerProxy": "0x3Bc6701cA1C32BBaC8D1ffA2294EE3444Ad93989",
        "WithdrawManager": "0xcBd99DfD6fbC55e7596318FC069bC3B7869Ff30a",
        "WithdrawManagerProxy": "0x3cf9aD3395028a42EAfc949e2EC4588396b8A7D4",
        "StakeManager": "0x0aEd86c6cA8c68C5499cec6F3570e2CA4860A918",
        "SlashingManager": "0xAb1e2218EAF1b2d242ddDD047BE5f5583A68BA84",
        "DelegationManager": "0xba032CD2B41a6FDA32ad9f1DE5623694a47Db9EA",
        "ExitNFT": "0xe4202974B2d5b2f26b7A8f27098EC439d1e6C4aa",
        "StateSender": "0x22E1f5aa1BA9e60527250FFeb35e30Aa2913727f",
        "predicates": {
          "ERC20Predicate": "0xaBE79B1B44581c69cCc45146dd8681Fb82a8AA18",
          "ERC721Predicate": "0x1F07Aa7eB46414d2F89746C7510E8597E82CF698",
          "MarketplacePredicate": "0x2E3a58bF3644E4D790f93A01527F85E211c57841",
          "TransferWithSigPredicate": "0x3f0dC47C79254cfCA4195519954b444F87a766E0"
        },
        "tokens": {
          "MaticWeth": "0x7BdDd37621186f1382FD59e1cCAE0316F979a866",
          "TestToken": "0x28C8713DDe7F063Fdc4cA01aB2A8856e0F243Fec",
          "TestERC721": "0x07d799252cf13c01f602779b4dce24f4e5b08bbd"
        }
      }
    }

### Matic
    "Matic": {
      "NetworkName": "Matic testnet",
      "ChainId": 15001,
      "RPC": "https://testnetv3.matic.network",
      "RPCWebSocketEndpoint": "wss://testnetv3-wss.matic.network",
      "SyncerAPI": "https://testnetv3-syncer.api.matic.network/api/v1",
      "Explorer": "https://testnetv3-explorer.matic.network",
      "DaggerEndpoint": "https://testnetv3-dagger.matic.network",
      "Contracts": {
        "ChildChain": "0xa2EF03edfA084ac9e5Bf110e409Ed5483BAe4101",
        "tokens": {
          "MaticWeth": "0x8567184E6F9b1B77f24AfF6168453419AD22f90e",
          "TestToken": "0x9a93c912F4eFf0254d178a18ACD980C1B05b57b0",
          "TestERC721": "0x8D5231e0B79edD9331e0CF0d4B9f3F30d05C47A5"
        }
      }
    }
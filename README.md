# Blockchain-Capstone_F
# Capstone: Real Estate Marketplace 
In this project i will be minting my own tokens to represent my title to the properties.
 Before you mint a token, you need to verify you own the property. 
 You will use zk-SNARKs to create a verification system which can prove you have title to the property without revealing that specific information on the property.

Once the token has been verified you will place it on a blockchain market place (OpenSea) for others to purchase. 


## Contract addresses on rinkeby test network and ABI
#### 1. Verifier 
```
 Deploying 'Verifier'
   --------------------
   > transaction hash:    0x7621142601c28d1893433da2a2c8eaf67c38e9a1e4bd8713ec0e
1a00127fd287
   > Blocks: 0            Seconds: 9
   > contract address:    0xEA76068437F4E54B72A08Aa5185e817E013844EF
   > block number:        7072446
   > block timestamp:     1598242517
   > account:             0x6c017cf603d1ECC3A4903262B296235b63B5e515
```
#### 2. SolnSquareVerifier
```
    Deploying 'SolnSquareVerifier'
   ------------------------------
   > transaction hash:    0xd6f266d544550dbcaf5cd8d209d020e4d2d15741800fcad53ac9
e93401219e0d
   > Blocks: 0            Seconds: 9
   > contract address:    0xC9a7447a432BBb91De7f582DB75414b4352E51F5
   > block number:        7072447
   > block timestamp:     1598242532
   > account:             0x6c017cf603d1ECC3A4903262B296235b63B5e515
```

### 3. Contract ABIs
 Can be found on `eth-contracts/build/contracts` folder of the project
 
## OpenSea MarketPlace Storefront link
- Original minter : `https://rinkeby.opensea.io/accounts/0x6c017cf603d1ecc3a4903262b296235b63b5e515`
- Buyer1 : `https://rinkeby.opensea.io/accounts/0xe06dc5c25cd66a7bcdc3b7a4c2e97f330cb95aaa`
Buyer2 : `https://rinkeby.opensea.io/accounts/0xf041ab72b92e3a694700c4e6176f6ba8657f8e3b`
Buyer3 : `https://rinkeby.opensea.io/accounts/0xc069535d28a3a4de3704cd73315bc133f9cc54af`
Buyer4 : `https://rinkeby.opensea.io/accounts/0x9f290910af622d435db6ff8013ea3f6b40efe06f`
Buyer5 : `https://rinkeby.opensea.io/accounts/0xc37e66d764fb9d3375b66c804b722b387fde2cbc`



### Prerequisites 

 - [NodeJS]
 - [ganache-UI]
 - [truffle]
 - MetaMask extension installed in your browser and few ethers on Rinkeby Test Network.
 - [Docker]

```
node -v
npm -v
npm i ganache-GUI -g
npm i truffle -g
```

## Technologies versions that were used 
	1. Truffle v5.1.29 (core: 5.1.29)
	2. Solidity - 0.5.5 (solc-js)
	3. Node v12.17.0
	4. Web3.js v1.2.1
	5. openzeppelin-solidity: ^2.2.0,

### Testing libraries
 - [chai](https://www.npmjs.com/package/chai)- assertion library for node.  
 - [truffle-assertions](https://www.npmjs.com/package/truffle-assertions) 


## Quick Start Deploying to Ganache and Testing

Clone this repository:

1. cd into project folder & install modules

        cd Blockchain-Capstone

        npm install

2. Compile Contracts

        truffle compile

1. Start ganache ( GUI)

            ganache-GUI

2. Mirgrate locally

              truffle migrate --reset 

#### Testing contracts

```Testing ERC721```

File: TestERC721Mintable.js

Test minting and transfering tokens functions.

    truffle test ./test/TestERC721Mintable.js

```Test zkSnarks```

File: TestSquareVerifier.js

Verifies zkSnarks is successfully implemented.

    truffle test ./test/TestSquareVerifier.js

```Testing ERC721 token with zkSnarks```

File: TestSolnSquareVerifier.js

Test minting with zkSnarks.

    truffle test ./test/TestSolnSquareVerifier.js


//``` You can also use the following command ```
	> truffle test    
		to test TestERC721Mintable, TestSquareVerifier and TestSolnSquareVerifier at one step
	

---
## Quick Start Deploying to Rinkeby

1. Make a new project with Infura

    Infura: https://infura.io

2. Setup truffle-config
	
	a. set mnemonic from metamask within HDWalletProvider 

    b. set infuraKey 

    c. set rinkeby endpoints within HDWalletProvider 


3. Migrate Verifier and SolnSquareVerifier to rinkeby test network

        truffle migrate --reset --network rinkeby

4. Finding ER721 token(EGY_House_Token) on ether-scan

  https://rinkeby.etherscan.io/token/0xc9a7447a432bbb91de7f582db75414b4352e51f5


5. Minting tokens

  https://www.myetherwallet.com/interface/interact-with-contract
  
  a. provide SolnSquareVerifier contract address (0xC9a7447a432BBb91De7f582DB75414b4352E51F5)
  b. provide SolnSquareVerifier contract ABI (`eth-contracts/build/contracts` folder of the project)
  c. start minting tokens


6. Finding ER721 token OpenSea MarketPlace 
	`https://rinkeby.opensea.io/assets?search=%7B%22query%22%3A%22egy_house_token%22%7D`

## Project assets on rinkeby opensea
	https://rinkeby.opensea.io/assets/0xc9a7447a432bbb91de7f582db75414b4352e51f5/1
	https://rinkeby.opensea.io/assets/0xc9a7447a432bbb91de7f582db75414b4352e51f5/2
	https://rinkeby.opensea.io/assets/0xc9a7447a432bbb91de7f582db75414b4352e51f5/3
	https://rinkeby.opensea.io/assets/0xc9a7447a432bbb91de7f582db75414b4352e51f5/4
	https://rinkeby.opensea.io/assets/0xc9a7447a432bbb91de7f582db75414b4352e51f5/5

## Author

 - Abdelrhman Younis


## Project Resources

* [Remix - Solidity IDE](https://remix.ethereum.org/)
* [Visual Studio Code](https://code.visualstudio.com/)
* [Truffle Framework](https://truffleframework.com/)
* [Ganache - One Click Blockchain](https://truffleframework.com/ganache)
* [Open Zeppelin ](https://openzeppelin.org/)
* [Interactive zero knowledge 3-colorability demonstration](http://web.mit.edu/~ezyang/Public/graph/svg.html)
* [Docker](https://docs.docker.com/install/)
* [ZoKrates](https://github.com/Zokrates/ZoKrates)

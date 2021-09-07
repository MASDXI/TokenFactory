# Advanced Sample Hardhat Project

Project directory structure
``` shell
.
├── contracts
│   ├── TokenERC1155.sol
│   ├── TokenERC20.sol
│   ├── TokenERC721.sol
│   ├── TokenERC777.sol.develop
│   └── TokenFactory.sol
├── coverage.json
├── docs
│   ├── ERC1155.md
│   ├── ERC20.md
│   ├── ERC721.md
│   └── ERC777.md
├── hardhat.config.js
├── LICENSE
├── package.json
├── package-lock.json
├── README.md
├── scripts
│   └── deploy.js
├── test
│   ├── erc1155.test.js
│   ├── erc20_capped.test.js
│   ├── erc20_unCapped.test.js
│   ├── erc721.test.js
│   ├── erc777.test.js
│   ├── factory.test.js
└── yarn.lock

```

This project demonstrates an advanced Hardhat use case, integrating other tools commonly used alongside Hardhat in the ecosystem.

The project comes with a sample contract, a test for that contract, a sample script that deploys that contract, and an example of a task implementation, which simply lists the available accounts. It also comes with a variety of other tools, preconfigured to work with the project code.

Try running some of the following tasks:

```shell
yarn clean
yarn compile
yarn coverage // coverage is unsport
yarn deploy-local
yarn deploy-prod
yarn verify
yarn test:erc20_capped
yarn test:erc20_unCapped
yarn test:erc721
yarn test:erc1155
yarn test:factory
yarn node
yarn help
REPORT_GAS=true npx hardhat test
npx eslint '**/*.js'
npx eslint '**/*.js' --fix
npx prettier '**/*.{json,sol,md}' --check
npx prettier '**/*.{json,sol,md}' --write
npx solhint 'contracts/**/*.sol'
npx solhint 'contracts/**/*.sol' --fix
```

# Etherscan verification

To try out Etherscan verification, you first need to deploy a contract to an Ethereum network that's supported by Etherscan, such as Ropsten.

In this project, copy the .env.template file to a file named .env, and then edit it to fill in the details. Enter your Etherscan API key, your Ropsten node URL (eg from Alchemy), and the private key of the account which will send the deployment transaction. With a valid .env file in place, first deploy your contract:

```shell
yarn deploy
npx hardhat run --network ropsten scripts/deploy.js
```

Then, copy the deployment address and paste it in to replace `DEPLOYED_CONTRACT_ADDRESS` in this command:

```shell
yarn verify
npx hardhat verify --network ropsten DEPLOYED_CONTRACT_ADDRESS "Hello, Hardhat!"
```

# Documents

- [ERC20](./docs/ERC20)  
- [ERC721](./docs/ERC721)  
- [ERC777](./docs/ERC777)  
- [ERC1155](./docs/ERC1155)  
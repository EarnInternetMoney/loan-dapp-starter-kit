# loan-dapp-starter-kit

This dapp is accompanied by a series of Medium articles to help developers get started with AZTEC.


The code base is split into 3 main folders.

1. client (The frontend react code that interfaces with web3 and graph-ql)
2. contracts (The solidity contracts deployed to ganache that interact with AZTEC)
3. graph (The graph-node mappings that index the local blockchain)


To get started

1. `git clone git@github.com:CreditMint/loan-dapp-starter-kit.git`
2. `cd loan-dapp-starter-kit`

3. `mv .env.test .env`

This copies the local file to a local .env file that ganache will use to deterministically create test accounts to make local development easier.

4. `cd client && yarn install`


5. `cd .. && yarn start`

The start script will do the following:
  • Start ganache, importing any accounts from the .env file
  • Compile and migrate both the dApp contracts and AZTEC and deploy the contracts the the local blockchain
  • Start a docker container that runs the graph-node
  • Build the graph-node mappings and deploy them to the graph-node
  • Copy the truffle build artefacts to the client for interaction with the contracts (ABIs)

6. In a new terminal window `yarn client`

This command will run the create-react-app and host the client at localhost:3000


Navigate to http://localhost:3000 and click the restore account button.

Ganache has been started with 3 deterministic development accounts, each funded with 1000 ETH (Wahoo). You can restore the first account by using the seed phrase `office shallow practice favorite diary review floor quote faith initial foot squeeze`.

Enter any password to encrypt the hot-wallet keystore vault and press restore to enter the dApp!




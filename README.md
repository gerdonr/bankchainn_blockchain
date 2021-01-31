
# Proof of Authority Development Chain (bankchainn)
For this assignment, I am taking on the role of a new developer at a small bank.
My mission is be to set up a testnet blockchain for your organization.
To do this, I will create and submit four deliverables:


 * Set up the custom testnet blockchain.


* Send a test transaction.


* Create a repository.


* Write instructions on how to use the chain for the rest of my team.



## Background
I have just landed a new job at ZBank, a small, innovative bank that is interested in exploring what
blockchain technology can do for them and their customers.
My first project at the company is to set up a private testnet that my team of developers and I 
can use to explore potentials for blockchain at ZBank.
I have decided on setting up a testnet because:
There is no real money involved, which will give my team of developers the freedom to experiment.
Testnets allows for offline development.
In order to set up a testnet, I am going to use the following skills/tools I learned in class:


* Puppeth, to generate your genesis block.


* Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.


* The Clique Proof of Authority algorithm.


Tokens inherently have no value here, so we will provide pre-configured accounts and nodes for easy setup.
After creating the custom development chain, create documentation for others on how to start it using the pre-configured
nodes and accounts. You can name the network anything you want, have fun with it!
Be sure to include any preliminary setup information, such as installing dependencies and environment configuration.

## Instructions for the Team

1) Setup the custom out-of-the-box blockchain


2) Create a new project directory for your new network. Call it whatever you want!


3) Create a "Screenshots" folder inside of the project directory.


4) Create accounts for two (or more) nodes for the network with a separate datadir for each using geth.


5) Run puppeth, name your network, and select the option to configure a new genesis block.


6) Choose the Clique (Proof of Authority) consensus algorithm.


7) Paste both account addresses from the first step one at a time into the list of accounts to seal.


8) Paste them again in the list of accounts to pre-fund. There are no block rewards in PoA, so you'll need to pre-fund.


9) You can choose no for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.


10) Complete the rest of the prompts, and when you are back at the main menu, choose the "Manage existing genesis" option.


11) Export genesis configurations. This will fail to create two of the files, but you only need networkname.json.


12) You can delete the networkname-harmony.json file.


13) Initialize each node with the new networkname.json with geth.


14) Run the first node, unlock the account, enable mining, and the RPC flag. Only one node needs RPC enabled.


15) Set a different peer port for the second node and use the first node's enode address as the bootnode flag.


16) Be sure to unlock the account and enable mining on the second node!


17) You should now see both nodes producing new blocks, congratulations!



## Send a test transaction


1) Use the MyCrypto GUI wallet to connect to the node with the exposed RPC port.


2) You will need to use a custom network, and include the chain ID, and use ETH as the currency.


3) Import the keystore file from the node1/keystore directory into MyCrypto. This will import the private key.


4) Send a transaction from the node1 account to the node2 account.


5) Copy the transaction hash and paste it into the "TX Status" section of the app, or click "TX Status" in the popup.


6) Screenshot the transaction metadata (status, tx hash, block number, etc) and save it to your Screenshots folder.


7) Celebrate, you just created a blockchain and sent a transaction!

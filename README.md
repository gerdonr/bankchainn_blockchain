
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

### Setup the custom out-of-the-box blockchain


1) Create a new project directory for your new network. Call it whatever you want!


2) Create a "Screenshots" folder inside of the project directory.


3) Create accounts for two (or more) nodes for the network with a separate datadir for each using geth.


4) Run puppeth, name your network, and select the option to configure a new genesis block.
![image](https://user-images.githubusercontent.com/63059287/106403676-dd8fda00-63fd-11eb-96fc-db749c46589e.png)


5) Choose the Clique (Proof of Authority) consensus algorithm.
![image](https://user-images.githubusercontent.com/63059287/106403743-1fb91b80-63fe-11eb-8450-d475db332586.png)

6) Paste both account addresses from the first step one at a time into the list of accounts to seal.


7) Paste them again in the list of accounts to pre-fund. There are no block rewards in PoA, so you'll need to pre-fund.


8) You can choose no for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.


9) Complete the rest of the prompts, and when you are back at the main menu, choose the "Manage existing genesis" option.


10) Export genesis configurations. This will fail to create two of the files, but you only need networkname.json.
![image](https://user-images.githubusercontent.com/63059287/106403797-5131e700-63fe-11eb-958c-3786aa6459bb.png)


11) You can delete the networkname-harmony.json file.


12) Initialize each node with the new networkname.json with geth.
![image](https://user-images.githubusercontent.com/63059287/106403857-8c341a80-63fe-11eb-861b-81d0a1ffe2d6.png)
**Initializing node1

![image](https://user-images.githubusercontent.com/63059287/106403878-abcb4300-63fe-11eb-85bd-d82d8e26cf39.png)
**Initializing node2

13) Run the first node, unlock the account, enable mining, and the RPC flag. Only one node needs RPC enabled.

Here, the --unlock flag unlocks the mine, the --mine flag tells the node to start mining, the --rpc flag enables the http-rpc server, and the --allow-insecure-unlock flag allows insecure account unlocking when account-related RPC's are exposed by http.
![image](https://user-images.githubusercontent.com/63059287/106403905-ce5d5c00-63fe-11eb-8a54-3a216012f86e.png)


14) Set a different peer port for the second node and use the first node's enode address as the bootnode flag.

Here we unlock node2 and select a different port. The --bootnodes flag allows for P2P discovery of the other node. 
![image](https://user-images.githubusercontent.com/63059287/106403942-e503b300-63fe-11eb-89d4-0c8ccfdef858.png)


15) Be sure to unlock the account and enable mining on the second node!


16) You should now see both nodes producing new blocks, congratulations!



## Send a test transaction


1) Use the MyCrypto GUI wallet to connect to the node with the exposed RPC port.


2) You will need to use a custom network, and include the chain ID, and use ETH as the currency.
![image](https://user-images.githubusercontent.com/63059287/106403956-f3ea6580-63fe-11eb-950a-6fb5b23e7485.png)


3) Import the keystore file from the node1/keystore directory into MyCrypto. This will import the private key.
![image](https://user-images.githubusercontent.com/63059287/106403973-0795cc00-63ff-11eb-84ba-b15273299064.png)


4) Send a transaction from the node1 account to the node2 account.
![image](https://user-images.githubusercontent.com/63059287/106404001-2a27e500-63ff-11eb-9c70-9723188becbd.png)


5) Copy the transaction hash and paste it into the "TX Status" section of the app, or click "TX Status" in the popup.


6) Screenshot the transaction metadata (status, tx hash, block number, etc) and save it to your Screenshots folder.
![image](https://user-images.githubusercontent.com/63059287/106403986-18ded880-63ff-11eb-8644-99e7fe88f049.png)


7) Celebrate, you just created a blockchain and sent a transaction!

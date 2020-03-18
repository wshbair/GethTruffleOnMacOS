
Geth Installation 
------------------
brew tap ethereum/ethereum
brew install ethereum //it install version 1.9.12-stable

Ethereum init
---------------
geth --rpc  --rpccorsdomain "*" --datadir "/Users/wazenshbair/geth-truffle/data" --port "30303" --nodiscover --networkid 3576 --nat "none" init "CommonGenesis.json"

Geth in Mining mode
------------------------
geth --rpc  --rpccorsdomain "*" --datadir "/Users/wazenshbair/geth-truffle/data" --port "30303" --nodiscover --networkid 3576 --nat "none" --allow-insecure-unlock --mine --minerthreads=8 --unlock 0 --password <(echo -n "123") --verbosity 0  console


Truffle side
------------
1. npm install // to install truffle 
2. truffle compile // compile smart contacts 
3. truffle migrate  // "2_deploy_contracts.js" is addedd in migration folder to deploy the helloworld.sol 


Results
--------
Starting migrations...
======================
> Network name:    'development'
> Network id:      3576
> Block gas limit: 0x7a1200


1_initial_migration.js
======================

   Replacing 'Migrations'
   ----------------------
   > transaction hash:    0xc696ca7cf4bb010512a9b583cf76d4e5b0ac4b881cb2da175bd31356963ce7c0
   > Blocks: 0            Seconds: 0
   > contract address:    0x5D78f5e6aA515950dF5DE2f5a37796EAaF61753a
   > block number:        58
   > block timestamp:     1584568522
   > account:             0x0b3A520eB398843FbC106f397c9D83dAdBF8A96C
   > balance:             295
   > gas used:            188483
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00376966 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00376966 ETH


2_deploy_contracts.js
=====================

   Deploying 'HelloWorld'
   ----------------------
   > transaction hash:    0x5a69373b660801a1966799254415358882c20648ff4ce2853ec2bde8c411ece9
   > Blocks: 0            Seconds: 0
   > contract address:    0x61964c8F0219Cd9885be249bC0DFcE1a6E0b8Bc8
   > block number:        62
   > block timestamp:     1584568526
   > account:             0x0b3A520eB398843FbC106f397c9D83dAdBF8A96C
   > balance:             310
   > gas used:            297052
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00594104 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00594104 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.0097107 ETH


# goethereum

Going through all the possible command line flags is out of scope here (please consult our CLI Wiki page), but we've enumerated a few common parameter combos to get you up to speed quickly on how you can run your own geth instance.

Hardware Requirements
Minimum:

CPU with 2+ cores
4GB RAM
1TB free storage space to sync the Mainnet
8 MBit/sec download Internet service
Recommended:

Fast CPU with 4+ cores
16GB+ RAM
High-performance SSD with at least 1TB of free space
25+ MBit/sec download Internet service
Full node on the main Ethereum network
By far the most common scenario is people wanting to simply interact with the Ethereum network: create accounts; transfer funds; deploy and interact with contracts. For this particular use case, the user doesn't care about years-old historical data, so we can sync quickly to the current state of the network. To do so:

$ geth console
This command will:

Start geth in snap sync mode (default, can be changed with the --syncmode flag), causing it to download more data in exchange for avoiding processing the entire history of the Ethereum network, which is very CPU intensive.
Start the built-in interactive JavaScript console, (via the trailing console subcommand) through which you can interact using web3 methods (note: the web3 version bundled within geth is very old, and not up to date with official docs), as well as geth's own management APIs. This tool is optional and if you leave it out you can always attach it to an already running geth instance with geth attach.

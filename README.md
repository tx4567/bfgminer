# BFGMiner
BFGMiner for Windows x64

This is the Ubuntu cross-compile Windows x64 from source https://github.com/luke-jr/bfgminer?tab=readme-ov-file

# Note: This is the text version and does not include the graphically menu/display***

Instructions for compiling both the source and dependencies will be provided soon.

This was compile as an object leason in mining solo against a full BTC node.

The command line used for mining was as follows:

>
> You BTC wallet must be a full node and synced.
> To ensure that the BTC node is setup to accept the communication, make sure the BITCOIN.CONF has the following:
> 

server=1      
prune=10000     
listen=1     
daemon=1     
rpcuser=abc     
rpcpassword=zzzzzzzzzz     
rpcallowip=127.0.0.1/255.255.255.0     
rpcport=8332     
rpcbind=127.0.0.1:8332


>
> Legacy addr: legacy BTC address - 
> open BTC Conole and enter the command ("solo legacy" is the address label, but what you want)
>
> getnewaddress "solo legacy" legacy 
> btc_legacy_address
>
bfgminer.exe -o http://127.0.0.1:8332 -u abc -p zzzzzzzzzz --coinbase-addr=btc_legacy_address --no-stratum -S all

NfyCoin (NFY)

This is a research COIN and should not be used for any other purpose.

Linux Ubuntu 12.04 x64:

sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

git clone https://github.com/nullifycoin/nullifycoin.git

cd nullifycoin

qmake-qt4 nfycoin-qt.pro

make
mkdir ~/.nfycoin
nano ~/.nfycoin/nfycoin.conf

Add this line:

addnode=162.243.242.178

addnode=184.154.13.230

./nfycoin-qt

GPU Mining

nfycoin.conf

-----------------

# Accept json-rpc commands

server=1

# Set username and password

rpcuser=mike

rpcpassword=kitties

# Allow RPC over port 9332

rpcport=9332

# Allow local ip's to connect

rpcallowip=127.0.0.1

rpcallowip=192.168.*.*

# Add these other users to confirm coins you found

addnode=162.243.242.178

addnode=184.154.13.230

# Don't attempte to generate litecoins using the wallet

gen=0

-----------------

Install cgminer-3.7.2, reaper, or another mining program

cgminer --scrypt -o localhost:9332 -u mike -p kitties




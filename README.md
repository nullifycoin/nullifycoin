## NfyCoin (NFY)

This is a research COIN and should not be used for any other purpose. Forked from litecoin in 2013.

Linux Ubuntu 12.04 x64:

```bash
sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev
git clone https://github.com/nullifycoin/nullifycoin.git
cd nullifycoin
qmake-qt4 nfycoin-qt.pro
make
mkdir ~/.nfycoin
echo "addnode=162.243.242.178" >> ~/.nfycoin/nfycoin.conf
echo "addnode=184.154.13.230" >> ~/.nfycoin/nfycoin.conf
./nfycoin-qt
```

## GPU Mining
### Config
```bash
cat > nfycoin.conf << EOF
# Accept json-rpc commands
server=1
# Set username and password
rpcuser=mike
rpcpassword=password
# Allow RPC over port 9332
rpcport=9332
# Allow local ip's to connect
rpcallowip=127.0.0.1
rpcallowip=192.168.\*.\*
# Add these other users to confirm coins you found
addnode=162.243.242.178
addnode=184.154.13.230
# Don't attempte to generate coins using the wallet miner
gen=0
EOF
```
### Mining
Install cgminer-3.7.2, reaper, or another mining program

```cgminer --scrypt -o localhost:9332 -u mike -p password -I 13```



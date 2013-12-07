NfyCoin (NFY)

This is a research COIN and should not be used for any other purpose.

Linux Ubuntu 12.04 x64
sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev git

git clone https://github.com/nullifycoin/nullifycoin.git

cd nullifycoin

qmake-qt4 nfycoin-qt.pro

make

cd src

make -f makefile.unix


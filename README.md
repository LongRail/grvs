GRVS Core (fork of PIVX) integration/staging repository
======================================

GRVS is an open source crypto-currency focused on fast private transactions with low transaction fees & environmental footprint.  It utilizes a custom Proof of Stake protocol for securing its network. The goal of GRVS is to achieve a decentralized sustainable crypto currency with near instant full-time private transactions.

- Anonymized transactions using the [_Zerocoin Protocol_](http://www.pivx.org/zpiv).
- Fast transactions featuring guaranteed zero confirmation transactions (_SwiftX_).
- Decentralized blockchain voting utilizing Masternode technology to form a DAO.

### Masternode Setup Guide

#### Masternode Setup Guide

It is recommended [use the shell script](https://github.com/grvscoindev/install_mn) to install a GRVS Masternode on a Linux server running Ubuntu

#### Quick installation of the GRVS daemon under linux

See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/grvscoindev/grvs.git
    cd GRVS
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip grvsd
    sudo strip grvs-cli
    sudo strip grvs-tx
    cd ..

Running the daemon:

`grvsd`

Stopping the daemon:

`grvs-cli stop`

Demon status:

`grvs-cli getinfo`

`grvs-cli mnsync status`

All binaries for different operating systems, you can download in the releases repository:

https://github.com/grvscoindev/grvs/releases

P2P port: 37821, RPC port: 37822
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.

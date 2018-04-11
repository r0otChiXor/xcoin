
Xcoin
============================
No premine. No IPO.

Specifications

    Block time: 60 seconds
    Difficulty retarget: every block
    Min transaction fee: 0.01 XCO
    Confirmations: 10, maturity: 100
    P2P port: 14641, RPC port: 14642


Proof of stake

    Min stake age: 8 hours, Max age 24 hours
    Block reward: 3% interest per year + 10 coins + transaction fees paid out every time you find a block
    Your reward before the fees is averaged up to the nearest 0.999
    Max reward 20 coins per block before the fees
    To maximize staking yield, combine your inputs after receiving a stake for 0.01 +fees
    0.01+fee reward means your inputs have split too much (or your input is too small). Send your coins back to your self to combine your inputs so you can have a bigger input. If you are staking a small amount of coins you will get this low reward too because the input is too small.
    Transaction fees are earned by block finders


Pools
https://www.ipominer.com/stats?curr=xco
https://xco.coin-miners.info/
https://xco.suprnova.cc

Wallets
Mac wallet: http://www.mediafire.com/download/2d1m2ib5mb2i3ie/Xcoin-Qt.zip
Windows wallet: https://mega.co.nz/#!mckS1QyC!JfD1SuaKGD0oQEFZPTuJTppy902a2bJ3jOuBa7TKHtI
Linux wallet: https://mega.co.nz/#!rdkESBBA!2joS-tyHxEnvqw2EaeWDk-5e21wZoXulUJIdcTi_Vlg
Source: https://github.com/el3ab/xcoin

Linux Build


    cd src/
    mkdir obj

    sudo apt-get update && apt-get upgrade
    sudo apt-get install ntp unzip git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev aptitude &&    aptitude install miniupnpc libminiupnpc-dev

    cd /xcoin/src/leveldb
    chmod +x build_detect_platform
    make clean
    make libleveldb.a libmemenv.a
    make -f makefile.unix 

CREATE CONFIG FILE

    nano ~/.Xcoin/Xcoin.conf

    Add the following, save and exit:

    daemon=1
    server=1
    rpcuser=(username)
    rpcpassword=(strong password)

Run Xcoind once more and if you did everything correctly, 
your daemon is now online! 

Type XCoind help for a full list of commands available.

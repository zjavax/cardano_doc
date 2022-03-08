# 测试网

准备工作
echo export SENDER="addr_test1qpwradmwwazdr6w6cxjmm9ptpy0835utgdufy06zjccycv0p7x6jmykac7xr5qwf8zca6mapkra282w4ganxjurkf02suyrzqe" >> $HOME/.bashrc
source $HOME/.bashrc
echo $SENDER

echo export CC_TEST1_RECEIVER="addr_test1qrz5nmt7cy7e2dpxsuf94kn8ztvacd7ys76dqmqc2fl23m3fqqgflwz7ahhqezd8mx5hfxmwh2stfagm8uwkxreya6rsdz4l8f" >> $HOME/.bashrc
source $HOME/.bashrc
echo $CC_TEST1_RECEIVER

发送的钱包地址
addr_test1qpwradmwwazdr6w6cxjmm9ptpy0835utgdufy06zjccycv0p7x6jmykac7xr5qwf8zca6mapkra282w4ganxjurkf02suyrzqe

接收的钱包地址
addr_test1qrz5nmt7cy7e2dpxsuf94kn8ztvacd7ys76dqmqc2fl23m3fqqgflwz7ahhqezd8mx5hfxmwh2stfagm8uwkxreya6rsdz4l8f

echo export CARDANO_NODE_SOCKET_PATH="CNODE_HOME/sockets/node0.socket" >> $HOME/.bashrc
source $HOME/.bashrc
cardano-cli query tip --testnet-magic 1097911063

currentSlot=$(cardano-cli query tip --testnet-magic 1097911063 | jq -r '.slot')
echo Current Slot: $currentSlot

cardano-cli query utxo \
--address $(cat payment.addr) \
--mainnet > fullUtxo.out





# 正式网
echo export SENDER="addr1qyw988ystej3jh4ue92rak383g9jt8wmqccy0gqjk4d69686jyexgjylx7knz65ag27yzdrh9gh9zskvsqzffhjulqyssej8rh" >> $HOME/.bashrc
source $HOME/.bashrc
echo $SENDER
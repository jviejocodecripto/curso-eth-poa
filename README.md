bootnode --genkey=boot.key



geth account new --datadir nodo --password pwd.txt

geth init --datadir nodo .\genesis.json

geth --authrpc.port 9553 --ipcpath "\\.\pipe\nodo" --datadir nodo --syncmode full --http --http.api "admin,eth,miner,net,personal" --http.port 9545 --allow-insecure-unlock --unlock "0x4458235bdf11e61187d2c2de342b226d99a85cd7" --password pwd.txt --nodiscover --mine 



--bootnodes "enode://c2da306e3afba5f0ecb022a0e35897f3a55c5accc4669a74ae7cb37ffd2cffd3f600363abec9edd2cd25040ab0f7bd978702f912220ecc6ab98df65b80066901@127.0.0.1:0?discport=30301" --port 30034 

geth --authrpc.port 9554 --ipcpath "\\.\pipe\nodo2" --datadir nodo2 --syncmode full --http --http.api "admin,eth,miner,net,personal" --http.port 9546 --allow-insecure-unlock --unlock "0x69ECb058E972c7555FC15cdBC7DF4Ec60b28c119" --password pwd.txt --nodiscover --mine --bootnodes "enode://c2da306e3afba5f0ecb022a0e35897f3a55c5accc4669a74ae7cb37ffd2cffd3f600363abec9edd2cd25040ab0f7bd978702f912220ecc6ab98df65b80066901@127.0.0.1:0?discport=30301" --port 30035

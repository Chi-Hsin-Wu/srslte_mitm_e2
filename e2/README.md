## E2 Termination
```
git clone
```
### 修改build_odu.sh中的ip及port
```shell=
export RIC_HOST="10.118.126.148"
export RIC_PORT=32511
export E2_SCTP_PORT=32500
export INTERFACE_TO_RIC="10.6.1.2"
export DEBUG=0
```
* RIC_HOST為跑setup-ric.sh時後面設的網卡的ip
* RIC_PORT對應到的32511是上面對腳本做修改的port
* E2_SCTP_PORT為這個e2 term要使用的sctp port，可做修改，不要衝突到就好
* INTERFACE_TO_RIC為e2 node的ip，要確保能夠跟RIC_HOST設的ip互通，要不然無法連上
### 編譯並執行
```
sudo ./build_odu.sh clean
sudo ./run_odu.sh
```
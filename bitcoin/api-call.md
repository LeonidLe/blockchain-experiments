1) Install full bitcoin node.


2) Configure the client:
~/.bitcoin/bitcoin.conf:
```
server=1
user=xxx
password=yyy
rcpport=8332
...
```

3) Test:
```bash
curl --user xxx:yyy --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getblockcount", "params": []}' \
     -H 'content-type: text/plain;' http://127.0.0.1:8332/
```

*Method*s (like **getblockcount**) are descibed here: https://developer.bitcoin.org/reference/rpc/index.html


4) Import private key
  - methd: **createwallet**
  - **importprivkey** (can take more than hour)
  
5) Create transaction:
   - steps:
       - **craeterawtransaction**
       - **signrawtransactionwithwallet**
       - **sendtoaddress**
       
   


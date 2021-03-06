# mincoin
Minimal Implementation of Blockchain and Cryptocurrency

```bash
~$ yarn install
~$ yarn start
```

## Test API
#### Get blockchain
```bash
~$ curl http://localhost:3001/blocks
```
#### Mine the first block with only a coinbase transaction
```bash
~$ curl -H "Content-type:application/json" --data "{\"data\" : [{\"txIns\":[{\"signature\":\"\",\"txOutId\":\"\",\"txOutIndex\":1}],\"txOuts\":[{\"address\":\"04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534a\",\"amount\":50}],\"id\":\"f089e8113094fab66b511402ecce021d0c1f664a719b5df1652a24d532b2f749\"}]}" http://localhost:3001/mineBlock
```
#### Query connected peers
```bash
~$ curl http://localhost:3001/peers
```
#### Add peer
```bash
~$ curl -H "Content-type:application/json" --data "{\"peer\":\"ws://localhost:6001\"}" http://localhost:3001/addPeer
```

## References
[Naivecoin](https://github.com/lhartikk/naivecoin)  
[Mastering Bitcoin: Programming the Open Blockchain 2nd Edition](https://github.com/bitcoinbook/bitcoinbook/blob/develop/README.md)  

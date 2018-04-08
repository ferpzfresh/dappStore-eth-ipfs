
`npm install` 

`ganache-cli` - run test rpc

`ipfs-daemon` - run ipfs 

`truffle migrate` - deploy contracts

`truffle console`

---

##### Truffle console interaction


Initialize account with ether
```language-javascript
  current_time = Math.round(new Date() / 1000);
  amt_1 = web3.toWei(1, 'ether');
``` 

Add products to store
```language-javascript
	EcommerceStore.deployed().then(function(i) {i.addProductToStore('Leather Bracelet', 'Handmade', 'QmfZmV5TSTMfJLxkSAe5GSgycR66vnrVDY4buppadJ5qXW', 'QmfZmV5TSTMfJLxkSAe5GSgycR66vnrVDY4buppadJ5qXW', current_time, current_time + (4*86400), amt_1, 0, {gas: 1000000, from: web3.eth.accounts[1]}).then(function(f) {console.log(f)})});
```

Check for item on blockchain
```language-javascript
	EcommerceStore.deployed().then(function(f) {f.getProduct.call(1).then(function(f) {console.log(f)})})
```
---
`npm run dev` - run application

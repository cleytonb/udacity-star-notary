IMPORTANT: Files `.secret` and `.infura` excluded for security purposes

---

Truffle version: v5.5.25

OpenZeppelin version: v2.3.0

ERC-721 Token Name: Cleyton StarNotary

ERC-721 Token Symbol: CSN

Rinkeby Token Address: 0x4e33DF5aF5Ad82818b3a636013869F842EC80191

---

OTHER NOTES

The openzeppelin version provided in the starter code does not have a constructor with name and symbol.

The starter code was not running the tests because on test was forcing the use of `gasPrice: 0` which doesn't work in current versions. But removing gasPrice causes the tests to break. The test in question makes a transaction to buy a star and compares the balance of the user who bought the star to see if it was charged correctly. I went to the starter code in github to see if there were any updates on this and saw a pull request, already approved, but not merged. I readed the code and understand it is getting the gas used in the method call and multiplying by the gas cost to calculate the total gas used to take it into account when comparing the balance before and after the transaction. Since I believe this is not directly relevant to the concepts being assessed, I copied this fix. In the test code I highlighted the piece of code taken from this pull request and referenced the author.

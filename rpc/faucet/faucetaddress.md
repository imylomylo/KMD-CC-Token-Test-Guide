## Find your own fauce address
Usage: `faucetaddress [pubkey]`

Example Command:
```shell
./komodo-cli -ac_name=ATEST faucetaddress 03fe754763c176e1339a3f62ee6b9484720e17ee4646b65a119e9f6370c7004abc
```
Output:
```JSON
{
  "result": "success",
  "FaucetCCaddress": "R9zHrofhRbub7ER77B7NrVch3A63R39GuC",
  "Faucetmarker": "RKQV4oYs4rvxAWx1J43VnT73rSTVtUeckk",
  "CCaddress": "RSxACZQhskPjQyxp7TUPG1oP1wm4agFycJ",
  "myCCaddress": "RJf8Hm6gcExTDvYkXi9Mvu9LjDuKkeewdq",
  "myaddress": "RGxBQho3stt6EiApWTzFZxDvqqsM8GwAuk"
}
```

**Help:**
```shell
komodo-cli -ac_name=ATEST help faucetaddress
faucetaddress [pubkey]
```
 - [ ] help faucet address todo

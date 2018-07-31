This is a Faucet smartcontract. Enabled anyone to setup and operate a faucet. There is a faucet address where everyone can send their funds and the address will be serving anyone who requests it.

## Available RPC Calls

== Faucet ==  
[faucetaddress [pubkey]](./faucetaddress.md) - will show you the faucet smart contract address  
[faucetfund amount](./faucetfund.md) - donate/send your funds to the faucet  
[faucetget](./faucetget.md) - request faucet funds  
[faucetinfo](./faucetinfo.md) - displays faucet funds balance


## Workflow

 - `komodo-cli -ac_name=ATEST faucetfund <amount>` (then decoderawtransaction, sendrawtransaction)
 - `komodo-cli -ac_name=ATEST faucetaddress <pubkey>`
 - `komodo-cli -ac_name=ATEST faucetget` (then decoderawtransaction, sendrawtransaction)

### Example

**faucetfund amount**
```shell
komodo-cli -ac_name=ATEST faucetfund 20
{
  "result": "success",
  "hex": "0100000002dfda72e45e0f85bb09378a25d5bed6f580f0137d169d5bcc9d3d010f2f2594810100000048473044022070e56e3f786e21cd3fcc2bf49e4db75cb742e3c64e5b6c87e6b9c074c05ebcd202202504ec96a606c34ac87f29593fe7c6e1f91fb0aee6fbf6d109c419e0a742e9a601ffffffffff18780b5081ce5f002e8f81090c6f2c2e639b365aef61b676f37d08fec23e8f010000006b483045022100bf4b04457e067357ffa9e02c749809ffe8fbdd979bf75985f43f6bbebb1f01d802204176cb0e0f30bb7f7c45d0663c8b0951482e6bd9611b1116964d38bdd2a2bfe6012103496adfde29629bf221ce383f141841d4de763132bfa38d05882f6f4122ba32e3ffffffff020094357700000000302ea22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401ccf0c532dd170900002321033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68cac00000000"
}
```
**decoderawtransaction hex**
```shell
removed
```
**sendrawtransaction hex**
```shell
removed
```

**faucetaddress pubkey**
 ```shell
 komodo-cli -ac_name=ATEST faucetaddress 03fe754763c176e1339a3f62ee6b9484720e17ee4646b65a119e9f6370c7004abc
{
  "result": "success",
  "FaucetCCaddress": "R9zHrofhRbub7ER77B7NrVch3A63R39GuC",
  "Faucetmarker": "RKQV4oYs4rvxAWx1J43VnT73rSTVtUeckk",
  "CCaddress": "RSxACZQhskPjQyxp7TUPG1oP1wm4agFycJ",
  "myCCaddress": "RJf8Hm6gcExTDvYkXi9Mvu9LjDuKkeewdq",
  "myaddress": "RGxBQho3stt6EiApWTzFZxDvqqsM8GwAuk"
}
 ```
**faucetget**
```shell
komodo-cli -ac_name=ATEST faucetget
privkey for the -pubkey= address is not in the wallet, importprivkey!
{ 
  "result": "success",
  "hex": "0100000001e7d8a125fcc9df2637f133c58cf33956ca4e746343b05a1303f257deae3791df000000007b4c79a276a072a26ba067a565802103682b255c40d0cde8faee381a1a50bbb89980ff24539cb8518e294d3a63cefe128140b465aa6bc5b563025bc1a1179f399e39be4d826c768a681ac0ae3db5ed6c8adc544dd88541434ffe70743bfc28ee50cd5e1851bbdc22142f3b532b3972c34b4ba100af038001e4a10001ffffffff02e0ae903c18090000302ea22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401cc00e1f505000000002321033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68cac00000000"
}
```

**decoderawtransaction hex**
```shell
komodo-cli -ac_name=ATEST decoderawtransaction 0100000001e7d8a125fcc9df2637f133c58cf33956ca4e746343b05a1303f257deae3791df000000007b4c79a276a072a26ba067a565802103682b255c40d0cde8faee381a1a50bbb89980ff24539cb8518e294d3a63cefe128140b465aa6bc5b563025bc1a1179f399e39be4d826c768a681ac0ae3db5ed6c8adc544dd88541434ffe70743bfc28ee50cd5e1851bbdc22142f3b532b3972c34b4ba100af038001e4a10001ffffffff02e0ae903c18090000302ea22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401cc00e1f505000000002321033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68cac00000000
{
  "txid": "8194252f0f013d9dcc5b9d167d13f080f5d6bed5258a3709bb850f5ee472dadf",
  "size": 275,
  "version": 1,
  "locktime": 0,
  "vin": [
    {
      "txid": "df9137aede57f203135ab04363744eca5639f38cc533f13726dfc9fc25a1d8e7",
      "vout": 0,
      "scriptSig": {
        "asm": "a276a072a26ba067a565802103682b255c40d0cde8faee381a1a50bbb89980ff24539cb8518e294d3a63cefe128140b465aa6bc5b563025bc1a1179f399e39be4d826c768a681ac0ae3db5ed6c8adc544dd88541434ffe70743bfc28ee50cd5e1851bbdc22142f3b532b3972c34b4ba100af038001e4a10001",
        "hex": "4c79a276a072a26ba067a565802103682b255c40d0cde8faee381a1a50bbb89980ff24539cb8518e294d3a63cefe128140b465aa6bc5b563025bc1a1179f399e39be4d826c768a681ac0ae3db5ed6c8adc544dd88541434ffe70743bfc28ee50cd5e1851bbdc22142f3b532b3972c34b4ba100af038001e4a10001"
      },
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 99996.99980000,
      "valueSat": 9999699980000,
      "n": 0,
      "scriptPubKey": {
        "asm": "a22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401 OP_CHECKCRYPTOCONDITION",
        "hex": "2ea22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401cc",
        "reqSigs": 1,
        "type": "cryptocondition",
        "addresses": [
          "R9zHrofhRbub7ER77B7NrVch3A63R39GuC"
        ]
      }
    },
    {
      "value": 1.00000000,
      "valueSat": 100000000,
      "n": 1,
      "scriptPubKey": {
        "asm": "033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68c OP_CHECKSIG",
        "hex": "21033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68cac",
        "reqSigs": 1,
        "type": "pubkey",
        "addresses": [
          "RGxBQho3stt6EiApWTzFZxDvqqsM8GwAuk"
        ]
      }
    }
  ]
}
```
**sendrawtransaction hex**
```shell
komodo-cli -ac_name=ATEST sendrawtransaction 0100000001e7d8a125fcc9df2637f133c58cf33956ca4e746343b05a1303f257deae3791df000000007b4c79a276a072a26ba067a565802103682b255c40d0cde8faee381a1a50bbb89980ff24539cb8518e294d3a63cefe128140b465aa6bc5b563025bc1a1179f399e39be4d826c768a681ac0ae3db5ed6c8adc544dd88541434ffe70743bfc28ee50cd5e1851bbdc22142f3b532b3972c34b4ba100af038001e4a10001ffffffff02e0ae903c18090000302ea22c8020e029c511da55523565835887e412e5a0c9b920801b007000df45e545f25028248103120c008203000401cc00e1f505000000002321033ace50aedf8df70035b962a805431363a61cc4e69d99d90726a2d48fb195f68cac00000000

faucetget validated
faucetget validated
8194252f0f013d9dcc5b9d167d13f080f5d6bed5258a3709bb850f5ee472dadf
```


## FAQ

**Q: So the faucet pubkey, is this a published thing that is given out by the "project" doing the faucet-ing?**

 - anybody can fund the faucet
 - faucetinfo shows how much funds it has
 - jl777cToday at 10:09 PM
 - each chain has only one faucet CC
 - presumably the community/project would fund it

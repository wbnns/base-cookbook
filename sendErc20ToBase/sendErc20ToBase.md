## Send approval transaction to the DAI ERC20 token contract to let the standard bridge contract spend the token:

```
cast send 0x6b175474e89094c44da98b954eedeac495271d0f --rpc-url
https://mainnet-infura.wallet.coinbase.com "approve(address,uint256)"
0x3154Cf16ccdb4C6d922629664174b904d80F2C35 1000000000000000000 --gas-limit
100000 --private-key <private key>
```

## Invoke bridgeERC20 on the L1StandardBridge contract for Base:

```
cast send 0x3154Cf16ccdb4C6d922629664174b904d80F2C35 --rpc-url
https://mainnet-infura.wallet.coinbase.com
"bridgeERC20(address,address,uint256,uint32,bytes)"
0x6b175474e89094c44da98b954eedeac495271d0f
0x50c5725949A6F0c72E6C4a641F24049A917DB0Cb 10000000000000000 150000 0x00
--gas-limit 200000 --private-key <private key>
```

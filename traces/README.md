
# mUSD

## Swap DAI for USDC

Example mUSD swap of DAI for USDC

[0x6136d94a6a4a2b616d58e08925fed839a5b6699c15c86f1a6cdfe0112e63fcb3](https://etherscan.io/tx/0x6136d94a6a4a2b616d58e08925fed839a5b6699c15c86f1a6cdfe0112e63fcb3)

![swap](./swap.png)

```tx2uml -x -v -g -a 0xca480d596e6717c95a62a4dc1bd4fbd7b7e7d705,0xafce80b19a8ce13dec0739a1aab7a028d6845eb3 -o swap 0x6136d94a6a4a2b616d58e08925fed839a5b6699c15c86f1a6cdfe0112e63fcb3```

# mAsset Save Wrapper

[SaveWapper](https://etherscan.io/address/0x0ca7a25181fc991e3cc62bac511e62973991f325#code) contract to facilitate deposits into the saving contract (imUSD) or imUSD Vault (v-imUSD).

## Save to imUSD Vault using USDC

Mint mUSD from USDC, deposit mUSD to savings contract (imUSD) and stake imUSD to imUSD Vault (v-mUSD).

![saveViaMintVault](./saveViaMintVault.png)

Generated from
```tx2uml -x -v -g -a 0xca480d596e6717c95a62a4dc1bd4fbd7b7e7d705,0xafce80b19a8ce13dec0739a1aab7a028d6845eb3 -f svg 0x3389ff9e3dd5ec8e06549d25f6c5c2c1c8b31ec4f24767186c497f9f8c827ddd -o saveViaMintVault```

# MTA Staking

## Create Lock
![mtaStakeCreate](./mtaStakeCreate.png)

```
tx2uml -x -v -g -o mtaStakeCreate 0xea06a71fbeae56849f3d79decad5f2214e1a7af2f051ac6522ba45e6251222ab
```

## Increase Lock
![mtaStakeIncreaseLock](./mtaStakeIncreaseLock.png)

```
tx2uml -x -v -g -o mtaStakeIncreaseLock 0x1c5485ef159bbe3c78be06205757913a3b3830d08eec5d51856c697c8ac46fb3
```
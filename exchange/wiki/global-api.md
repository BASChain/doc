# Global APIs


## load DApp Configuration

> When DOM listener MetaMask injected and get network chainId we load DApp Configuration Items

### Configuration Items

| key  | volume examples (data type) | Default | Comments  |
|  ----  |  ---- | ---- | ---- |
|  symbol | BAS (string) | BAS  | -- |
|  decimals | 18 (int) | 18 | -- |
|  rareGas  | 2000*10**18 (string bignumber) | 2000*10**18 | Rare Root Domain BAS wei |
|  topGas  | 200*10**18 (string bignumber) | 200*10**18 | Common Root Domain BAS wei |
|  subGas  | 4*10**18 (string bignumber) | 4*10**18 | Applied Sub Domain Cost BAS wei (Default)  |
|  externalGas  | 100*10**18(string bignumber) |  100*10**18  | To open public Cost BAS wei |
|  maxYearReg  |  5(int)  |  5  | -- |
| maxDaysReg  | 157680000 (int)  |  157680000  | -- |
|  ...  |  ---- |  -- |  -- |

> API 

```javascript 
loadConfiguration(chainId,{options})

return Promise() or callback

```

> chainId (required :network id )

0x03 or 3 

> options (Optional)

```json
{
  ...
}
```

###

# Global APIs

## set global web3 provider

> when DApp DOM loaded will set SDK web3 provider

> ?


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

## load balances

> When DApp listener watched MetaMask login then load balances

### API 

> Methods loadBalances(chainId,wallet,options={})

> Request Params 

```bash
chainId:3,                      //required
wallet:'0xaf..0fd8a',           //required
options: {                      //Optional
  web3js,
}
```

> Return Object 

```js
{
  ethBalance:12.23456*10**18 ,  //ETH wei(string)
  basBalance:10000*10**18,      //BAS wei(string)
  drawWei:125*10**18,           //Draw Balance (string)
}
```

## findDomain

> find Domain by string 

> Methods 

findDomain(
params={
  qstr:'',                      //required, like 'eth' 'eth.io',''
  chianId:3,                    //required 
},options={                     //Optional
  web3js
})

> Return Object 

```js 
{
  state:1,                                        //1 has result ,0 no result
  error:'',                                       // when state 0 ,error can set error msg like qstr Illegal ed. (like qstr 'eth.okex&_')
  domain:{                                        // when state 0 ,no this data
    name:'eth',
    owner:'0x23..',
    hash:'0xdf....',
    expire:157473723,
    isRoot:true,
    openApplied:true,
    isCustomed:true,
    customPrice:'1250000000000000000000',         // Custom defined price (wei)
  },
  root:{                                          //state = 1 and parent domain exist
    name:'eth',
    owner:'0x123...',
    hash:'0xdf....',
    expire:157473723,
    isRoot:true,
    openApplied:true,
    isCustomed:true,
    customPrice:'1250000000000000000000',         // Custom defined price (wei)    
  },
  dns:{                                           //state = 1 
    ipv4:['',''],                                 //if ipv4 not set value=[]
    ipv6:['',''],                                 //if ipv6 not set value=[]
    ...
  }
}
```

## getDomain

> get Domain Details by hash 

<font style="color:red">if unfound maybe throw Error</font>

> methods 

```js 
getDomainByHash(params={
  hash:'0xad...',                                   //required 
  chainId:3                                         //required
},options = {
  web3js,
})
```

> Return Object 

```js 
{
  state:1,                                        //state = 1 success , state =0 fail
  error:'not found',                              //state = 0 
  domain:{                                        // when state 0 ,no this data
    name:'eth',
    owner:'0x23..',
    hash:'0xdf....',
    expire:157473723,
    isRoot:true,
    openApplied:true,
    isCustomed:true,
    customPrice:'1250000000000000000000',         // Custom defined price (wei)
  },
  root:{                                          //state = 1 and parent domain exist
    name:'eth',
    owner:'0x123...',
    hash:'0xdf....',
    expire:157473723,
    isRoot:true,
    openApplied:true,
    isCustomed:true,
    customPrice:'1250000000000000000000',         // Custom defined price (wei)    
  },
  dns:{                                           //state = 1 
    ipv4:['',''],                                 //if ipv4 not set value=[]
    ipv6:['',''],                                 //if ipv6 not set value=[]
    ...
  }    
}
```


# Domain Apply Module

## GetRareDomains 

> getRootDomains(qstr)

Use Server API

## findDomain 

> findDomain(params={
  qstr:'',
  chainId
},
options={
  web3js
})

> See Global API Docs [Goto](./global-api.md##findDomain)


## Check Allownce for regist 
> check approve allownce token for regist 

### Methods 

> checkAllownceForApply(spender,chaindId,options={
  web3js
})

> Params 
```js 
spender:'0xad...',                                  //required current login address
chainId:3,                                          //required
options:{                                           // Optional
  web3js
}
```


> return true or false                              //if return true not need approve

## Evalue Apply Root Domain Cost Wei 

> Methods 

```js 
evalueRootCost(
params={
  domaintext:'',                                        // required punycode hanlde text string
  years:1,                                              // required
  isCustomed:false,                                     // required
  chainId:3,                                            // required
},
options={
  web3js                                                // Optional
})
```

> Return Object (Promise) 
```js
{
  domaintext:'',
  costWei:'20000000000000000000000'                     // if valid success value must
}
```

> throw Error Code : See Error Code 
```
if valid false throw Error() or return Promise.reject(10001)
```

## Evalue Apply Sub Domain Cost Wei

> ....



##  Approve Token

> Methods 

```js
approveForApplyEmitter(
params={
  wallet,                                           //required 
  chainId,                                          //required
  costWei                                           //required
},options={
  web3js
})

```

## Regist Root Domain 

> Method 

```js 
registRootEmitter(
  params={
    domaintext:'',                                      //required
    openApplied:true,                                   //required
    isCustomed:true,                                    //required
    customPrice:'20000000000000000000000000',           //required
    years:1,                                            //required
    chainId:3,                                          //required
  },options={
    wallet:'0x8afde...fa67'                              //Optional
    web3js,                                              //Optional
  })
```

> return function 

** Emitter Function  **

## Regist Sub Domain 

> Methods 

```js 
registSubEmitter (
  params={
    roottext:'',                                          //required rootDomain text string (handle.trim().toLowerCase())
    subtext:'',                                           //required subdomain text string (handle trim().toLowerCase())
    years:1,
    chainId:3,
    wallet:''
  },
  options:{
    web3js
  })
```
> return function 

** Emitter Function  **




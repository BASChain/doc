# Wallet APIs 

## GetMySubDomains

> Methods 

```js 
getMySubDomains(params={
  pagenumber:1,                                       //required
  pagesize:20,                                        //required
  wallet:''                                           //required
  chainId:3,                                          //required
},options={
  web3js
})
```

> Return Object (Promise)

```js 
{
  state:1,
  wallet:'0xaf..0fd8a',
  total:58,
  items:[                                               // if state=0  items = []
    {
      name:'',                                          //
      domaintext:'',                                    // handle by punycode
      hash:'',
      owner:'',                                         // for fonter changed wallet valid
      expire:15725363,
      isorder:true,                                     // is market on sale
    }
  ]
}
``` 

## GetMyRootDomains

> Methods 

```js 
getMyRootDomains(params={
  pagenumber:1,                                       //required
  pagesize:20,                                        //required
  wallet:''                                           //required
  chainId:3,                                          //required
},options={
  web3js
})
```

> Return Object (Promise)

```js 
{
  state:1,
  wallet:'0xaf..0fd8a',
  total:58,
  items:[                                               // if state=0  items = []
    {
      name:'',                                          //
      domaintext:'',                                    // handle by punycode
      hash:'',
      owner:'',
      expire:15725363,
      isorder:true,                                     // is market on sale
      isCustomed:false,
      openApplied:true,
      customPrice:'40000000000000000000000'             // if openApplied = true  customPrice need set value (wei) 
    },
    ...
  ]
}
``` 

## Get My OnSale Domains 

> Methods

```js
getMyOnSaleDomains(params={
  pagenumber:1,
  pagesize:20,
  wallet:'',
  chainId:3
},options={
  web3js
})
```

> Return 

```js
{
  state:1,
  pagenumber:1,
  total:56,
  wallet:'',
  items:[
    {
      name:'',
      domaintext:'',                                    // domain handle by punycode
      hash:'',
      owner:'',                                         //use for when fonter changed wallet ,the operator button can't used
      isRoot:true,
      ordertime:1576425,
      price:'200000000000000000000',                    // Market price (wei)
    },
    ...
  ]
} 
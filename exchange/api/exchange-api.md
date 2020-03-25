# BAS Website API

## Domain 

### 1. 获取钱包下的所有购买的domain的总数

> url : /api/domain/getDomainTotal

  * method: POST
  * request

```json
{
  "wallet":"0x3D002404deee63697fBEf95657DcE57335BF561D"
}
```

 * response

```json
{
  "state":1,
  "data":13  
}
```

### 2.获取钱包下的所有购买的domain 列表

> url : /api/domain/getDomainList

  * method: POST
  * request

```json
{
  "wallet":"0x3D002404deee63697fBEf95657DcE57335BF561D",
  "pageNumber":1,
  "pageSize":18
}
```

 * response

```json
{
  "state":1,
  "owner":"0x3D002404deee63697fBEf95657DcE57335BF561D",
  "data":[
    {
      "name":"liao",
      "expire":1583734806,
      "openApplied":false,
      "hash":"0xa4256546741ae78e509e2168486b5c8ae64998a485bcc5c8492fcf9cd980b351"
    },     
    {
      "name":"exp.liao",
      "expire":1583734806,
      "openApplied":false,
      "hash":"0xbbedd4056f47fbaba43a75eaa4d0b42db6be8e4f35f955fc69ab26d5e2c25a69
    },
    {
      "name":"1.liao",
      "expire":1615274987,
      "openApplied":false,
      "hash":"0xd60b3c9e2f93aff041bfbb099f5372ae2fd21ebae7ce4b7d83ff675a1ca78c8b"
    }
  ]
}
```  

### 4.转出域名时，当用户输入域名时，自动补全

> url : /api/domain/domainSell

  * method: POST
  * request

```js
{
  "text":"e",
  "wallet":"0x3D002404deee63697fBEf95657DcE57335BF561D"
}
//或者
{
  "text":"e"
}
```

 * response

```json
{
  "state":1,
  "domainhashpair":[
    {
      "domainname":"exp.cai",
      "walletaddress":"0x9ccCbDe29DeED16c9d88415259c27cdf9368A5A2",
      "expire":1583734806
    },
    {
      "domainname":"eth.lws",
      "walletaddress":"0xea8a3a416799d582bC46987E084886524E7449Df",
      "expire":1615704506
    }
  ]
}
```


## DApp State Initial Interface 
> DApp 状态参数初始化接口

> url /api/dappstate/getInit

  * method: POST/GET
  * request

```js 
{

}
```

> Response

``` js 
{
  state:1,
  data:{
    symbol:'BAS',
    decimals:18,
    rareGas:500*(10**18),
    topGas:20*(10**18),
    subGas:4*(10**18),
    customedPriceGas:100*(10**18),
    maxYearReg:5,
    aliasMaxLen:256,
    extrainfoMaxLen:512    
  }
}
```
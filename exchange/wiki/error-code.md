# Error Codes

> SDK Error Code length 4 

> DApp Error Code length 6

## Code Maps

### SDK Code 

|  Code  |  Name  |  DESC  |  Comments  |
|  ----  |  ----  |  ----  |  ----  |
|  1000  |  noweb3 | not set web3js provider |  ---- |
|  1001  | nologin | MetaMask not login,no wallet or chainId | ---- |
|  1002  | lackOfEthBalance  | Lack of ETH balance | ----  |
|  1003  | lackOfBasBalance  | Lack of BAS balance | ----  |
|  1004  | ...  |  ---- |  ---- |
|  ...   | ...  |  ----  | ---- |
|  2000  | record exist | data exist on blockchain  |  ---- |
|  ...   | ...          | ----  |  ----  |
|  3001  | unsupportNetwork  |  unsupport network  | ----  |
|  4001  | userDeadedAuthorize | MetaMask Rejected or User cancel request |  ---- |


### DApp Code 

|  Code  |  Name  | DESC  |  Comments  |
|  ----  |  ----  |  ---- |  ---- |
|  111111  | paramsIllegal  | request parameter illegal |  method  |
|  100000  | ...            | ....    |  ---- | 
|  200001  | domainExist  | domain exist on blockchain  | ---- |
|  200002  | lackOfBalance | domain evalCost validator fail | ---- |
|  200003  | rootNotOpenApply | root domain not open to public | ---- |
|  200004  | domainNotOpenEmail  | domain not open mail regist | ---- |
|  999999  | bizFailure  |  excute bussiness logic fail | ---- |



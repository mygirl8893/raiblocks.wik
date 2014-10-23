The RPC protocol accepts JSON http requests.  The following are RPC commands along with the responses that are expected.

## Send  
Request:  
`{  
  "action": "send",  
  "account": "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8",
  "amount": "1000000"  
}`  
Response:  
`{  
  "sent": "1"  
}`

## Account balance  
Request:  
`{  
  "action": "account_balance",  
  "account": "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"  
}`  
Response:  
`{  
  "balance": "0"  
}`

## Account create  
Request:  
`{  
  "action": "wallet_create",  
}`  
Response:  
`{  
  "account" : "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"  
}`

## Wallet contains  
Request:  
`{  
  "action": "wallet_contains",  
  "account": "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"  
}`  
Response:  
`{  
  "exists" : "1"
}`

## Wallet list  
Request:  
`{  
  "action": "wallet_list"  
}`  
Response:  
`{  
  "accounts" : [
  "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"  
  ]
}`

## Wallet add  
Request:  
`{  
  "action": "wallet_add",  
  "key": "34F0A37AAD20F4A260F0A5B3CB3D7FB50673212263E58A380BC10474BB039CE4"  
}`  
Response:  
`{  
  "account" : "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"
}`

## Validate account number checksum  
Request:  
`{  
  "action": "validate_account",  
  "account": "U63Kt3B7yp2iQB4GsVWriGv34kk2qwhT7acKvn8yWZGdNVesJ8"  
}`  
Response:  
`{  
  "valid" : "1"
}`
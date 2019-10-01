OAuth Flow

### Authorization Code Flow

#### Request Format
```
https://<Domain>/authorize
?client_id=fffffff
&redirect_uri=https://oauthdebugger.com/debug
&scope=offline_access openid
&response_type=code
&response_mode=query
&nonce=enuwzvjzjc
```

#### Note  offline_access is used so that when authorization_code grant type will be used with token end point it will return refresh token

Response
```
dAkf9eR93rOocohP
```

#### Authorization Code Grant Type

#### Request
```
curl -X POST \
  https://igtb-sdu.auth0.com/oauth/token \
  -H 'Cache-Control: no-cache' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Postman-Token: e3a80b8c-6d9c-4557-8c7d-fb35a64b969b' \
  -d 'grant_type=authorization_code&
      client_id=FASDFSDA&
      code=7tTAZVs81ZtVwuiM&
      redirect_uri=https%3A%2F%2Foauthdebugger.com%0A      
```


#### Client Credential Grant Type

#### Request
```
curl -X POST \
  https://<Domain>/oauth/token \
  -H 'Cache-Control: no-cache' \
  -H 'Content-Type: application/x-www-form-urlencoded' \  
  -d 'grant_type=client_credential&
   client_id=ggggg&
   client_secret=fasdfasdf&
   redirect_uri=https%3A%2F%2Foauthdebugger.com%0A&   
```



#### Refresh TOken Grant type

```
curl -X POST \
  https://igtb-sdu.auth0.com/oauth/token \
  -H 'Cache-Control: no-cache' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Postman-Token: 750f9f97-7ede-4aaa-bdf1-6edcf5d53623' \
  -d 'grant_type=refresh_token&client_id=43dCuXEJuvEzt4tPtU9ClZi1QS-dYdeQ&refresh_token=hDO9Y354OOj1jPnwyAZVXc13dSM3w1DsfVnlw_68ceNfh'
```  

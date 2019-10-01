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

#### Client Credential Flow

Clinet credential flow can be two type with user context without user 
with user grant type will be `authorization_code` and without user it woutl be `client_credential`

#### Request
```
curl -X POST \
  https://<Domain>/oauth/token \
  -H 'Cache-Control: no-cache' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Postman-Token: 6acea452-3b8e-4a36-b82d-33bf2b44e57c' \
  -d 'grant_type=authorization_code&client_id=ggggg&client_secret=fsfddssdf&redirect_uri=https%3A%2F%2Foauthdebugger.com%0A&audience=https%3A%2F%2Fsdu-53%2Fapi%2F'

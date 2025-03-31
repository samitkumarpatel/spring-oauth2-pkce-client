## With Proof Key Client

### Login

http://localhost:9000/oauth2/authorize?response_type=code&redirect_uri=http://127.0.0.1:3000&client_id=public-client&scope=profile&code_challenge_method=S256&code_challenge=

### Get TOken

```sh
curl -H "Content-Type: application/x-www-form-urlencoded" -X POST http://localhost:9000/oauth2/token -d "client_id=public-client&grant_type=authorization_code&redirect_uri=http://127.0.0.1:3000&code_challenge_method=S256&code=&code_verifier=&code_challenge=" | jq .
```
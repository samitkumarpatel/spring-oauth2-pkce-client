

## Without Proof Key

http://localhost:9000/oauth2/authorize?response_type=code&client_id=client_1&redirect_uri=http://1ocalhost:3000&scope=openid

```sh
curl -u "client_1:secret_1" -H "Content-Type: application/x-www-form-urlencoded" -X POST http://localhost:9000/oauth2/token -d
"grant_type=authorization_code&code=QgnfZhGy9uAAUY8F®UyWXMeHxZYHhCEw®5Eg-®pI661QQTiTybFFZiORausKBNr®XRZJ-2оZV3_ptipEDXLFC1[07HYcRUnkrGzvnRmk2sHI3LZ_8
_KLMDqGFrD8D-sn&redirect_uri=http://localhost:3000"
```

## With Proof Key Client

http://localhost:9000/oauth2/authorize?client_id=public-client&scope=openid+profile&redirect_uri=http://127.0.0.1:3000&response_type=code&code_challenge_method=S256&code_challenge=sQeA2sOpej8efz9xnRq9JeE8KdleW_5xQZtCnhnJWEM


```sh
curl -u "public-client:public-secret" -H "Content-Type: application/x-www-form-urlencoded" -X POST http://localhost:9000/oauth2/token -d "grant_type=authorization_code&redirect_uri=http://127.0.0.1:3000&Code=jkPJV5kMILXFIYYr0GrcadW7W-FQEwCBGiXJ4kQ7LsOnGjZ8l7r5WaNxXneBr-yI_CL7TzfTCBRXX6rYBotBy92W34g1HbiEpbHqmZBfB8fqc996uv7szeimn_TY3uAW&code_verifier=62uq9_Fx6iQI2yOXoKURyyw-DybR87OHrgeMRDuE-dk"
```

http://localhost:9000/oauth2/authorize?response_type=code&client_id=public-client&scope=profile&code_challenge=Zwy31mbC2SlVCH9_y2T79egwOXU7fcR5Wus5Rv6tLSs&code_challenge_method=S256&code_verifier=SoUn8Mepoc5wiXE_z84OlpbsYIi-vY_Fjrjih18EusE&redirect_uri=http://127.0.0.1:3000


```sh
curl -u "public-client:public-secret" -H "Content-Type: application/x-www-form-urlencoded" -X POST http://localhost:9000/oauth2/token -d "grant_type=authorization_code&redirect_uri=http://127.0.0.1:3000&Code=Hiy6Ai_hEtEUMFa4AzaHjzLKrH7qsK9rwSf77-ngVfRSRh5DMmcnBuk8fdoSDjcV5TbSe_UocE9k8iDmu_oNdUnA6PK31O4pcGAbGdZ4kB-aS3HsS9Td0IDYd1Fob12o&code_verifier=SoUn8Mepoc5wiXE_z84OlpbsYIi-vY_Fjrjih18EusE&code_challenge=Zwy31mbC2SlVCH9_y2T79egwOXU7fcR5Wus5Rv6tLSs&client_id=public-client&code_challenge_method=S256" | jq .
```
## With Proof Key Client

### Login

http://localhost:9000/oauth2/authorize?response_type=code&client_id=public-client&scope=profile&code_challenge=Zwy31mbC2SlVCH9_y2T79egwOXU7fcR5Wus5Rv6tLSs&code_challenge_method=S256&code_verifier=SoUn8Mepoc5wiXE_z84OlpbsYIi-vY_Fjrjih18EusE&redirect_uri=http://127.0.0.1:3000

### Get TOken

```sh
curl -u "public-client:public-secret" -H "Content-Type: application/x-www-form-urlencoded" -X POST http://localhost:9000/oauth2/token -d "grant_type=authorization_code&redirect_uri=http://127.0.0.1:3000&Code=Hiy6Ai_hEtEUMFa4AzaHjzLKrH7qsK9rwSf77-ngVfRSRh5DMmcnBuk8fdoSDjcV5TbSe_UocE9k8iDmu_oNdUnA6PK31O4pcGAbGdZ4kB-aS3HsS9Td0IDYd1Fob12o&code_verifier=SoUn8Mepoc5wiXE_z84OlpbsYIi-vY_Fjrjih18EusE&code_challenge=Zwy31mbC2SlVCH9_y2T79egwOXU7fcR5Wus5Rv6tLSs&client_id=public-client&code_challenge_method=S256" | jq .
```
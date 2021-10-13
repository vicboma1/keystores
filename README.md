# keystores

```
Generate keystore from certificate

1 - keytool.exe -import -trustcacerts -keystore application.keystore -storepass DDDDD -alias XXXXX -file file.cer

2 - keytool.exe -list -v -keystore application.keystore -storepass DDDDD


Import an existing x509 certificate and private key in java keystore to PKCS12

1 - openssl pkcs12 -export -in file.crt -inkey file.key -out server.p12 -name server -CAfile ca.crt -caname root -chain

2 - ../../../Archivos\ de\ programa/Java/jdk11.0.9/bin/keytool -importkeystore -deststorepass DDDDD -destkeypass EEEEE -destkeystore application.keystore -srckeystore server.p12 -srcstoretype PKCS12 -srcstorepass ZZZZZZZ -alias XXXX 

3 - keytool.exe -list -v -keystore application.keystore -storepass YYYYY  | grep -B 3 "PrivateKeyEntry\|SecretKeyEntry"

```

# HTTPS-Certificate-Example
Create selfsign certificate using JKS keytool for HTTPS/TLS communication, among different Spring Boot applications.


# To generate self sign certificate:
==================================

# Step 1: goto your jre bin folder
C:\Program Files\Java\jre1.8.0_121\bin

# Step 2: Then run below command:
keytool -genkey -alias https-example -storetype JKS -keyalg RSA -keysize 2048 -validity 365 -keystore https-example.jks

Or use below command
====================
keytool -genkeypair -alias sibsankar-example -storetype JKS -keyalg RSA -keysize 2048 -validity 365 -keystore sibsankar-example.jks

# Step 3:
After generation of https-example.jks certificate, copy it and put it in your spring boot application resources directory.

# To view the generated jks certificate use below command:
keytool -list -v -keystore https-example.jks

# To generate secret key use below command: 
keytool -genseckey -alias sibs-example -storetype jceks -keyalg AES -keysize 256 -validity 365 -keystore sibs-example.jks

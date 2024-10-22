
# Signed-Pdf-Info-Viewer

This project extracts the digital signature of the signed PDF and displays each piece of information.

## Digital Signature Process
![image](https://github.com/user-attachments/assets/5792fb6d-55c2-4d0b-9d7a-a33cc02f6551)

## You Can View..
<h4> 1. CMS Signed Data </h4>
Cryptographic Message Syntax (CMS).  This syntax is used to digitally sign, digest, authenticate, or encrypt arbitrary message content.
The CMS specification Cryptographic Message Syntax [CMS] is based on PKCS#7 version 1.5 and ties down some of its ambiguities.

<h4> 2. MessageDigest </h4>
A message digest is a fixed size numeric representation of the contents of a message. The message digest is computed by a hash function and can be encrypted, forming a digital signature.

<h4> 3. Pdf Hash Value </h4>
A PDF Hash Value is calculated from upload PDF document. Typically, this value is same with the message digest included in the digital signature statement

<h4> 4. SignedAttributes </h4>
https://datatracker.ietf.org/doc/html/rfc5652#section-11

This section defines attributes that may be used with signed-data, enveloped-data, encrypted-data, or authenticated-data.

<h4> 5. PublicKey </h4>
It is a certificate public key for decrypting the signature encrypted with the signature's certificate private key at the time of signing included in the CMS.

<h4> 6. Encryption SignedAttributes </h4>
Signed Attributes encrypted with the signer's certificate private key.

<h4> 7. Decryption SignedAttributes </h4>
Signed Attributes decrypted with the signer's certificate public key. In general, this value matches the Signed Attributes extracted above.

## This is Page Sample
![image](https://github.com/user-attachments/assets/aa0972ed-88a2-4ea4-9dea-64f76f7aa226)


## Running the server in Docker Container ##
##### Docker #####
Command to build the container :

```
docker build . --tag signed-pdf-info-viewer
```

Command to run the container :

```
docker run -p 3000:3000 signed-pdf-info-viewer
```

##### Docker Compose #####
Another alternative to run the application is to use the docker-compose.yml file and utility. To build the application using docker-compose simply execute the following command :
```
docker-compose build
```

And to run the application, please execute the following command :
```
docker-compose up
```

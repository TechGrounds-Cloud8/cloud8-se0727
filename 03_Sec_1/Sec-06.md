## Public Key Infrastructure

Public key cryptography works as follows: Public Key Infrastructure (PKI) uses a pair of keys to achieve the underlying security service. The key pair comprises of private key and public key.
If you know my public key (what I look like) you can use it to see me across the network. You could send me a message. I can sign your message and send you my signature. Verifying that signature is the evidence you’re talking to me. This effectively allows computers to see who they’re talking to across a network. 

What if you don’t know my public key? That’s what certificates are for.

A **certificate** is a data structure that contains a public key and a name. 
The data structure is then signed. The signature binds the public key to the name. The entity that signs a certificate is called the **issuer (or certificate authority = CA)** and the entity named in the certificate is called the **subject**.

If the issuer (or CA) signs a certificate for Bob, that certificate can be interpreted as the statement: “The issuer (or CA) says Bob’s public key is 01:23:42…".This is a claim made by the issuer (or CA)about Bob. The claim is signed by the issuer (or CA), so if you know the issuer (or CA)’s public key you can authenticate it by verifying the signature. If you trust the issuer (or CA) you can trust the claim.

Certificates let you use trust and knowledge of an issuer’s public key to learn another entity’s public key

You can relate it to your driver license = certificate
Issuer or CA = stadhuis gemeente

#### Key Management
There are two specific requirements of key management for public key cryptography.
* Secrecy of private keys: secret keys must remain secret from all parties except those who are owner and are authorized to use them.
* Assurance of public keys: PKI provides assurance of public key. It provides the identification of public keys and their distribution. 


### PKI exists of the following components:

#### Public Key Certificate, commonly referred to as ‘digital certificate’.
Digital certificates are based on the ITU standard X.509, sometimes also referred to as X.509 certificates.

Public key pertaining to the user client is stored in digital certificates by The Certification Authority (CA) along with other relevant information such as client information, expiration date, usage, issuer etc.

CA digitally signs this entire information and includes digital signature in the certificate.

Anyone who needs the assurance about the public key and associated information of client carries out the signature validation process using CA’s public key. Successful validation assures that the public key given in the certificate belongs to the person whose details are given in the certificate.

![alt text](../00_includes/Sec/Sec6/sec-06%20The%20process%20of%20validating%20in%20PKI.PNG)


#### Certifying Authority (CA)

The CA issues certificate to a client and assist other users to verify the certificate. The CA takes responsibility for identifying correctly the identity of the client asking for a certificate to be issued, and ensures that the information contained within the certificate is correct and digitally signs it.

Key Functions of CA are as follows:

* Generating key pairs 
* Issuing digital certificates  − the CA issues a certificate after client provides the credentials to confirm his identity. The CA then signs the certificate to prevent modification of the details contained in the certificate.

* Publishing Certificates 

* Verifying Certificates − The CA makes its public key available in environment to assist verification of his signature on clients’ digital certificate.

* Revocation of Certificates − At times, CA revokes the certificate issued due to some reason such as compromise of private key by user or loss of trust in the client.

4 Classes of Certificates

Class 1 − These certificates can be easily acquired by supplying an email address.

Class 2 − These certificates require additional personal information to be supplied.

Class 3 − These certificates can only be purchased after checks have been made about the requestor’s identity.

Class 4 − These may be used by governments and financial organizations needing very high levels of trust.


#### Registration Authority.

CA may use a third-party Registration Authority (RA) to perform the necessary checks on the person or company requesting the certificate to confirm their identity.

#### Certificate Management System (CMS).
 
It is the management system through which certificates are published, temporarily or permanently suspended, renewed, or revoked. Certificate management systems do not normally delete certificates because it may be necessary to prove their status at a point in time, perhaps for legal reasons. A CA along with associated RA runs certificate management systems to be able to track their responsibilities and liabilities.

#### Private Key Tokens
While the public key of a client is stored on the certificate, the associated secret private key can be stored on the key owner’s computer. This method is generally not adopted. If an attacker gains access to the computer, he can easily gain access to private key. For this reason, a private key is stored on secure removable storage token access to which is protected through a password.

Different vendors often use different storage formats for storing keys. For example, Entrust uses the proprietary .epf format, while Verisign, GlobalSign, and Baltimore use the standard .p12 format.

#### Hierarchy of CA

The CA is the center of the PKI, so the relationship of CA systems, both to each other (CA hierarchy) and to other subsystems (security domain) is vital to planning a Certificate System PKI.

When there are multiple CAs in a PKI, the CAs are structured in a hierarchy or chain. The CA above another CA in a chain is called an root CA; a CA below another CA in the chain is called a subordinate CA. A CA can also be subordinate to a root outside of the Certificate System deployment; for example, a CA which functions as a root CA within the Certificate System deployment can be subordinate to a third-party CA.

![alt text](../00_includes/Sec/Sec6/sec-06%20Three%20lvl%20CA%20hierarchy.PNG)

***
### Key terminology

* PKI
* CA
* Certificate
* Subject


***
### Exercise and Results

* ## Create a self-signed certificate on your VM.

### How to create a self-signed SSL Certificate using the OpenSSl tool on Ubuntu Linux.

Prerequisites
The OpenSSL toolkit is required to generate a self-signed certificate.

To check whether the openssl package is installed on your Linux system, open your terminal, type **openssl version**, and press Enter. If the package is installed, the system will print the OpenSSL version, otherwise you will see something like openssl command not found.


To create a new Self-Signed SSL Certificate, use the openssl req command. Below is the command to generate a SSL/TLS certificate for the example.com domain.
openssl req -newkey rsa:4096 -x509 -sha256 -days 365 -nodes -out example.crt -keyout example.key

The command details are as followed:

* -newkey rsa:2048 – creates a new certificate request and 2048 bit RSA key.
* -x509 – creates a X.509 certificate.
* -sha256 – use 265-bit SHA (Secure Hash Algorithm) to create the certificate
* -days 365 – the number of days to certify the certificate for. Typically a year or more
* -nodes – creates a key without a passphrase.
* -out example.crt – specifies the filename to write the newly created certificate to
* -keyout example.key – specifies the filename to write the private key to.

Once you press ENTER, the command will generate a private key and prompt you with series of questions to use to generate the certificate.


![alt text](../00_includes/Sec/Sec6/sec-06%20creating%20certificate%20and%20key.PNG)

Generating a RSA private key
...................................++++
............................++++
writing new private key to 'example.key'
-----
You’ll provide these answers similar to the ones below. Replace details with your own that represent the certificate you’re generating.

Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:New York
Locality Name (eg, city) []:New York
Organization Name (eg, company) [Internet Widgits Pty Ltd]:EXAMPLE, Inc.
Organizational Unit Name (eg, section) []:Publishing
Common Name (e.g. server FQDN or YOUR name) []:example.com
Email Address []:admin@example.com


After that, two files (example.crt and example.key) will be created in the directory you ran the command. Use these file in your Nginx or Apache setup to enable HTTPS connections.

The certificate and private key will be created at the specified location. Use the ls command to verify that the files were created:

 $ ls

Output
example.crt example.key

![alt text](../00_includes/Sec/Sec6/sec-06%20creating%20certificate%20and%20key%20part2.PNG)



* ## Analyze some certification paths of known websites (ex. techgrounds.nl / google.com / ing.nl).

When you open a browser and type in  the name of the site u like to visit u will see a "lock"button left of the url. When u click on the lock, than connection is secured, than certificate is valid and as last click on th etab Certification Path, u will see for Google has been signed by GlobalSign and Techgrounds has been signed by DigiCert Baltimore, and ING has been signed by Entrust.net.

![alt text](../00_includes/Sec/Sec6/sec-06%20certpath%20Techgrounds.PNG)

![alt text](../00_includes/Sec/Sec6/sec-06%20certpath%20Google.PNG)

![alt text](../00_includes/Sec/Sec6/sec-06%20certpath%20ING.PNG)





* ## Find the list of trusted certificate roots on your system (bonus points if you also find it in your VM).
*  Windows and Linux

Managing Trusted Root Certificates in Windows 10 and 11
How to see the list of trusted root certificates on a Windows computer?

To open the root certificate store of a computer running Windows 11/10/8.1/7 or Windows Server 2022/2019/2016, run the mmc.exe console;
Select File -> Add/Remove Snap-in, select Certificates (certmgr) in the list of snap-ins -> Add;
Select that you want to manage certificates of local Computer account;
Next -> OK -> OK;
Expand the Certificates node -> Trusted Root Certification Authorities Store. This section contains the list of trusted root certificates on your computer.

![alt text](../00_includes/Sec/Sec6/sec-06%20list%20of%20trusted%20cert%20windows.PNG)

![alt text](../00_includes/Sec/Sec6/sec-06%20list%20of%20trusted%20cert%20windows%20part2.PNG)



Most distros put their certificates soft-link in system-wide location at /etc/ssl/certs. For system-wide use, OpenSSL should provide you /etc/ssl/certs and /etc/ssl/private.

gebruik: ls dus ls /etc/ssl/certs

![alt text](../00_includes/Sec/Sec6/sec-06%20list%20of%20trusted%20cert%20linux%20VM.PNG)


***
### Sources

https://www.tutorialspoint.com/cryptography/public_key_infrastructure.htm

https://learn.hashicorp.com/tutorials/vault/pki-engine

https://smallstep.com/blog/everything-pki/

https://www.encryptionconsulting.com/certificate-authority-and-hierarchy/

https://websiteforstudents.com/how-to-create-self-signed-certificates-on-ubuntu-linux/

https://linuxize.com/post/creating-a-self-signed-ssl-certificate/

https://devopscube.com/create-self-signed-certificates-openssl/

http://woshub.com/updating-trusted-root-certificates-in-windows-10/#h2_1

https://docs.microsoft.com/en-us/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#to-view-certificates-for-the-current-user

https://unix.stackexchange.com/questions/97244/list-all-available-ssl-ca-certificates

https://serverfault.com/questions/62496/ssl-certificate-location-on-unix-linux

***
### Overcome challenges






### 

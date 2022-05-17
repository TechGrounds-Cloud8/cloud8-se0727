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

The process of obtaining Digital Certificate by a person/entity is depicted in the following illustration.

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
### Exercise

* Create a self-signed certificate on your VM.
* Analyze some certification paths of known websites (ex. techgrounds.nl / google.com / ing.nl).
* Find the list of trusted certificate roots on your system (bonus points if you also find it in your VM).



***
### Sources

https://www.tutorialspoint.com/cryptography/public_key_infrastructure.htm

https://learn.hashicorp.com/tutorials/vault/pki-engine

https://smallstep.com/blog/everything-pki/

https://www.encryptionconsulting.com/certificate-authority-and-hierarchy/


***
### Overcome challenges






### Results

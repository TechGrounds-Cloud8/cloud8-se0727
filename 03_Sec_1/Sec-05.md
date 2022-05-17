## Asymmetric encryption

What is the difference between symmetric and asymmetric encryption?

Symmetric encryption uses a private key to encrypt and decrypt an encrypted email.
Asymmetric encryption uses the public key of the recipient to encrypt the message. Then if the recipient wants to decrypt the message the recipient will have to use his/her private key to decrypt. If the keys correspond then the message is decrypted.

Summary Public key cryptography

* Public key cryptography provides the basis for securely sending and receiving messages with anyone whose public key you can access.
 
* Public keys enable:
    * Users to encrypt a message to other individuals on the system
    * You can confirm a signature signed by someone’s private key
* Private keys enable:
    * You can decrypt a message secured by your public key
    * You can sign your message with your private key so that the recipients know the message could only have come from you.


Generating public and private keys

The public and private key are not really keys but rather are really large prime numbers that are mathematically related to one another. Being related in this case means that whatever is encrypted by the public key can only be decrypted by the related private key.
 
A person cannot guess the private key based on knowing the public key. Because of this, a public key can be freely shared. The private key however belongs to only one person.

RSA(Rivest-Shamir-Adleman) is an Asymmetric encryption technique that uses two different keys as public and private keys to perform the encryption and decryption. With RSA, you can encrypt sensitive information with a public key and a matching private key is used to decrypt the encrypted message. Asymmetric encryption is mostly used when there are 2 different endpoints are involved such as VPN client and server, SSH, etc.

***
## Key terminology

* Public Key
* Private Key
* RSA
  


***
## Exercise and Results

* Generate a key pair.
  
  ![alt ext](../00_includes/Sec/Sec3/sec-05%20generate%20key%20pair%2C%20send%20public%20key%20to%20peer.PNG)

* Send an asymmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key you share with them. The recipient should be able to read the message, but it should remain a secret to everyone else.

![alt text](../00_includes/Sec/Sec3/sec-05%20mijn%20boodschap%20nr%20peer.PNG)

I used the public key of my peer to encrypt a message. Which i posted to him on SLack. And which he could decrypt.(using his private key and  the encrypted message).


![alt text](../00_includes/Sec/Sec3/sec-05%20encrypt%20boodschap%20van%20peer.PNG)

This is the encrypted message my peer send to me, using my public key.
I used my private key and the encrypted message to decipher the message and see the output of the communication .

* You are not allowed to use any private messages or other communication channels besides Slack. 
  
* Analyse the difference between this method and symmetric encryption.

With this method of encryption using key pairs (public and private), it is possible to send messages over a public channel.
Because other people can not have or get to your private keys. In contrast to Sec-4 symmeric encryption where the key was also given and easy to decrypt a message.


***
### Sources


https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange#:~:text=The%20Diffie%E2%80%93Hellman%20key%20exchange%20method%20allows%20two%20parties%20that,using%20a%20symmetric%2Dkey%20cipher.

https://travistidwell.com/jsencrypt/demo/ key pair generator

https://www.devglan.com/online-tools/rsa-encryption-decryption\ key pair generator with possibility to enter own text.

https://www.preveil.com/blog/public-and-private-key/


***
### Overcome challenges

U need to know the idea behind the keys (public and private) and how/when to use them

***


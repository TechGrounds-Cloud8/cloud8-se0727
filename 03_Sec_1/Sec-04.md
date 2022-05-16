## Symmetric Encryption

What is Cryptography?
Cryptography is the study of secure communications techniques that allow only the sender and intended recipient of a message to view its contents. The term is derived from the Greek word kryptos, which means hidden. It is closely associated to encryption, which is the act of scrambling ordinary text into what’s known as ciphertext and then back again upon arrival.


What is Cipher?
In cryptography, a cipher (or cypher) is an algorithm for performing encryption or decryption. To encipher or encode is to convert (encrypt) information (by a series of well-defined steps that can be followed as a procedure) into cipher or code.

**symmetric key algorithms**
T he same key is used for both encryption and decryption. The key must be known to the recipient and sender and to no one else.

**asymmetric key algorithms**
A different key is used for each. The enciphering key is different from, but closely related to, the deciphering key. If one key cannot be deduced from the other, the asymmetric key algorithm has the public/private key property and one of the keys may be made public without loss of confidentiality.

Caesar Cipher

Caesar cipher:
Method in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet. The method is named after Julius Caesar, who used it in his private correspondence.

Scytale
Scytale Was A Simple Cipher Used By The Spartans
Scytale was an ancient form of encryption commonly in ancient/classical Greece. It is a form of transposition cipher where letters are re-arranged in the messages prior to being deciphered by the recipient. 

This method involved the use of a cylinder around which a parchment was wrapped and the message written onto it. The recipient would use a rod of the exact same dimensions to read the message.

Given its simplicity, it was easily decipherable by the enemy too. 

 The Enigma Code 
 The term 'Enigma Code' is generally understood as the cipher device used by German forces during WW2 to encrypt their transmissions.


## Modern Ciphers used today

* Block Cipher
A block cipher is a deterministic algorithm operating on fixed-length groups of bits, called blocks. They are specified elementary components in the design of many cryptographic protocols and are widely used to the encryption of large amounts of data, including data exchange protocols. It uses blocks as an unvarying transformation.

* Transport Layer Security (TLS)
is a cryptographic protocol designed to provide communications security over a computer network. The protocol is widely used in applications such as email, instant messaging, and voice over IP, but its use in securing HTTPS remains the most publicly visible.

    The TLS protocol aims primarily to provide cryptography, including privacy (confidentiality), integrity, and authenticity through the use of certificates, between two or more communicating computer applications. It runs in the application layer and is itself composed of two layers: the TLS record and the TLS handshake protocols.



***
## Key terminology

Cryptography
Cipher
Caesar cipher
Basic of cryptography: symmetric encryption



***
## Exercise

* Find two more historic ciphers besides the Caesar cipher.
* Find two digital ciphers that are being used today.
* Send a symmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key you share with them. Try to think of a way to share this encryption key without revealing it to everyone. 
You are not allowed to use any private messages or other communication channels besides Slack. Analyse the shortcomings of this method.


Running Key Cipher

The Algorithm 
The 'key' for a running key cipher is a long piece of text, e.g. an excerpt from a book. The running key cipher uses the following tableau (the 'tabula recta') to encipher the plaintext:

![alt text](../00_includes/Sec/Sec3/sec-04%20symmetric.PNG)

To encipher a message, write the key stream above the plaintext: 

plaintext: Dit is de boodschap aan Ismail voor de opdracht sec04. stuur een bevestiging als je het snapt.

key: Onze sleutel is dit die we gebruiken voor het coderen want dat heb je nodig om te kunnen encrypten

Onze sleutel is dit die we gebruiken voor het coderen want dat heb je nodig om te kunnen encrypten
Dit is de boodschap aan Ismail voor de opdracht sec04. stuur een bevestiging als je het snapt.

So, the ciphertext for the plaintext is:

rvsmkoivhsoaukiidirewsejcpwyvqzcduyevjhvitwgquexhnulzfbxvulvmoxlnobrgwaecv

![alt text](../00_includes/Sec/Sec3/sec-04%20symmetric%20cyphertext.PNG)

![alt text](../00_includes/Sec/Sec3/slack%20sec-04%20delen%20key.PNG)


Het is onmogelijk om de key niet herkenbaar te maken via symmetric encryptie.

***
### Sources

https://cryptii.com/pipes/caesar-cipher

https://interestingengineering.com/11-cryptographic-methods-that-marked-history-from-the-caesar-cipher-to-enigma-code-and-beyond

https://www.laits.utexas.edu/~anorman/BUS.FOR/course.mat/SSim/life.html

https://medium.com/@prashanthreddyt1234/real-life-applications-of-cryptography-162ddf2e917d

https://en.wikipedia.org/wiki/Public-key_cryptography

https://www.tutorialspoint.com/cryptography/advanced_encryption_standard.htm

https://www.trentonsystems.com/blog/symmetric-vs-asymmetric-encryption

https://www.thesslstore.com/blog/symmetric-encryption-algorithms/  Sec-05

https://www.websiterating.com/nl/cloud-storage/what-is-aes-256-encryption/

https://www.cryptomathic.com/news-events/blog/symmetric-key-encryption-why-where-and-how-its-used-in-banking




***
### Overcome challenges


***
### Results

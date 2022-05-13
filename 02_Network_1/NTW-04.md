## Counting in Binary and Hex



The Decimal System
The decimal number system is the one that we are most familiar with, we use it every day. Decimal is what we refer to as a positional number system. That is, the position of the digits gives meaning to the value they represent. The other number systems (binary, hexadecimal and octal) are also positional, so once we understand the underlying theory of decimal we can easily apply that to understand the other systems.

Let's look at an example:

If I have the number 31415, what this actually represents is:

30,000 + 1,000 + 400 + 10 + 5

Or more precisely:

3 * 104	30,000
1 * 103	1,000
4 * 102	400
1 * 101	10
5 * 100	5

Decimal is base 10. This means we have 10 symbols for representing values ( 0 - 9 ). As we move through each position we multiply that number by 10 to the power of that position (starting at 0 at the far right side).


Binary
Binary follows the same pattern as Decimal except that instead of being base 10, it is instead base 2. Instead of having 10 symbols to represent values we have two ( 0 and 1 ).

So Decimal is a base 10 number system, we have 10 symbols and multiply by powers of 10. It follows that Binary is a base 2 number system, we have two symbols and multiply by powers of 2.

Let's look at an example:

If I have the binary number 101010, this translates into decimal as:

32 + 0 + 8 + 0 + 2 + 0 = 42

Or:

1 * $2^$5 25 |	32

0 * 24 | 	0
1 * 23 | 8
0 * 22 | 	0
1 * 21 |	2
0 * 20 |	0

As you can see from this example, binary is not as convenient as decimal for humans to read and work with. So you may be asking, Why bother with binary then? The answer is that it is an easier format for computers to work with. It may also be utilised in other areas as a shortcut to represent settings.


Hexadecimal

Hexadecimal is base 16

For hexadecimal we go up to 15 (remember we start from 0). Once we get to 9 we add the letters of the alphabet A - F to represent 10 - 15 (see the reference table below).

Let's take the decimal number 27.

In hexadecimal this would be 1B which in decimal translates into:

1 * 161 + 11 * 160 = 16 + 11




***
## Key terminology

Systems:
* Binary system
* Decimal System
* HexaDecimal System

***
## Exercise and Results

*  Translate the following decimal numbers into binary:

Decimal | Binary
--------|-------
16 | 0001 0000
128 | 1000 0000
228 | 1110 0100
112 | 0111 0000
73 | 0100 1001

* Translate the following binary numbers into decimal:

Binary | Decimal
-------|--------
1010 1010 | 170
1111 0000 | 240
1101 1011 | 219
1010 0000 | 160
0011 1010 | 58

* Translate the following decimal numbers into hexadecimal:

Decimal | Hex
------- | -------
15 | F
37 | 25
246 | F6
125 | 7D
209 | D1

 * Translate the following hexadecimal numbers into decimal:

Hex | Decimal
------- | -------
88 | 136
E0 | 224
CB | 203
2F | 47
D8 | 216




***
### Sources for Counting in base 2 and base 16


https://www.youtube.com/watch?v=FFDMzbrEXaE

https://www.youtube.com/watch?v=QJW6qnfhC70

https://www.youtube.com/watch?v=R8bdSWiBsfw

https://www.youtube.com/watch?v=bt4zavZCrLg

http://www.steves-internet-guide.com/binary-numbers-explained/

https://ryanstutorials.net/binary-tutorial/

https://jaantollander.com/post/scientific-writing-with-markdown/

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

https://learninglab.gitlabpages.inria.fr/mooc-rr/mooc-rr-ressources/module1/ressources/introduction_to_markdown.html#exponents-and-indices


***
### Overcome challenges


***
### 

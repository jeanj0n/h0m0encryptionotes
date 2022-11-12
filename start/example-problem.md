---
description: picoCTF :)
---

# Example Problem



{% embed url="http://mercury.picoctf.net:34962/" %}

The following CTF uses the principle of homomorphic encryption applied on cookies

![](<../.gitbook/assets/image (23).png>)

The auth\_name is double base64 encoded and the letters C, B and C are capitalized in the description, giving us a hint that this would be subject to a CBC bit flip attack

![](<../.gitbook/assets/image (22).png>)

Essentially, the point is that we cannot directly modify the cookie directly and manipulate it to our liking in this problem, without the hint we would have no clue how to approach this. The data present to us directly is encrypted and all operations happen in the background.


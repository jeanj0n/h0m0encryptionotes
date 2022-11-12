---
description: Not related really but was nice to include
---

# Diffie Hellman

**Key exchange, not encryption/decryption**

Consider a prime number q

Select any **α** such that **α\<q** and **α** is primitive root

### Primitive Root

**α**^1,2.....q-1 mod q should have values {1,2,3,....q-1} need not be in order just the values should be there

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

### Private Key (Xa)

Assume any value for Xa where Xa\<q

**Now Public Key Ya = α^Xa mod q**

Similarly, Assume Xb - Private only

Public Key Yb = **α^Xb mod q**

**Notice α and q are same for both, only the Xa and Xb we assume is different**

### **Calculate Secret Keys**

Generate two keys K1 and K2 for person A and B respectively.

**K1 = (Yb)^Xa mod q**

**K2 = (Ya)^Xb mod q**

**If K1 = K2, then success, happy days**


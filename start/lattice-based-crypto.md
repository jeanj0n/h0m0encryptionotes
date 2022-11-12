---
description: post quantum crypto sols
---

# Lattice Based Crypto

Lattice : Any regularly spaced grid of points stretching out to infinity. For example, here are 2 different, 2-dimensional lattices.

Basis : A small collection of vectors that can be used to reproduce any point in the grid that forms the lattice.

Vector :  Is nothing more than a fancy name for a point, a tuple of numbers called the _coordinates_ of the vector.

Previous crypto formulas were based on factorization of very large numbers eg. RSA. However it isn't quantum safe and such schemes would break down easily.&#x20;

In this, we would be given a basis containing large vectors (very distant from the origin) and will be asked to find a small vector close to the origin.

Using vector addition, the number of possibilities are endless and the probability of cracking this by bruteforcing is basically zero.

{% embed url="https://medium.com/cryptoblog/what-is-lattice-based-cryptography-why-should-you-care-dbf9957ab717" %}
Main Extract
{% endembed %}

{% embed url="https://www.techtarget.com/searchsecurity/definition/Diffie-Hellman-key-exchange" %}

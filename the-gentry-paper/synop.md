# Synop

[https://www.cs.cmu.edu/\~odonnell/hits09/gentry-homomorphic-encryption.pdf](https://www.cs.cmu.edu/\~odonnell/hits09/gentry-homomorphic-encryption.pdf)

An algorithm is said to have **polynomial time complexity** if its worst-case running time **T**worst(n) for an input of size n is upper bounded by a polynomial p(n) for large enough n≥n0

A homomorphic encryption scheme E has **four algorithms**: KeyGen**ε** , Encrypt**ε**, Decrypt**ε** and Evaluate**ε** all of which must be efficient – that is, run in time poly(λ),

**Seeing if evalE is efficient**

Sf < (k · Tf · log Tf) \[Sf is size of boolean circuit required to compute function f, Tf is time taken to run function f in Turing machine]

“Hard” means that any algorithm or “adversary” A that runs in poly(λ) time has a negligible probability of success over the choices of pk and m (i.e., the probability it outputs m is less than (1/λ^k)

#### Semantically Secure

&#x20; If an encryption scheme is deterministic – i.e., if there is only one ciphertext that encrypts a given message – then it cannot be semantically secure. An attacker can easily tell whether c encrypts m0, by running c0 ← Encrypt(pk, m0) and seeing if c and c0 are the same.&#x20;

A semantically secure encryption scheme must be probabilistic – i.e., there must be many ciphertexts that encrypt a given message, and Encrypt**ε** must choose one randomly according to some distribution.

###

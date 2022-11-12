# Basics

The basic idea to accomplish FHE scheme is to introduce noise purposely to the ciphertext to make it difficult to extract the valid data from noisy ciphertexts.

We evaluate circuits (a bunch of gates hooked together) where the inputs are the encrypted ciphertext(s) and the output is also a ciphertext.&#x20;

### Why NAND gates

AND OR and NOT are the only boolean operations you need to compute any boolean expression. With one NAND gate, we can express those three operations by changing input expression. Hence, it is functionally complete and is used in evaluation of circuits

![](<../.gitbook/assets/image (20).png>)

### Bootstrapping

> &#x20;A $$C$$-evaluation scheme is called _bootstrappable_ if it is able to homomorphically evaluate its own decryption circuit plus one additional NAND gate.

These circuits generate noise and after a certain threshold, it can't be decrypted anymore. Gentry invented “bootstrapping” which is to “refresh” the ciphertext to ensure the correctness of decryption.

He showed that by taking the decryption algorithm for his scheme and converting it into a circuit and passing the circuit a ciphertext and an encrypted version of the private key, you would get a ciphertext of the same plaintext, but with the noise gone. Furthermore, the cipher allowed you to run at least one NAND gate on two ciphertexts (a couple of gates that were equivalent to a NAND) and the decryption circuit without the noise being too much.

Suppose we want to execute&#x20;

```
(A NAND B) NAND (C NAND (D NAND A))
```

We can do this by adding the decryption circuit (DEC) after every NAND operation to ensure minimal noise.

```
DEC(
  DEC(
    A NAND B
  ) 
  NAND 
  DEC(
    C NAND 
    DEC(D NAND A)
  )
)
```

Since Gentry called the encryption scheme before bootstrapping “somewhat” homomorphic, this SWHE term remains in all the later works. All the scheme of FHE  should contain a SWHE (supports only limited depth of evaluation circuit ie. limited number of operations), plus proper noise management in the ciphertext.

{% embed url="https://crypto.stackexchange.com/questions/42666/what-exactly-is-bootstrapping-in-fhe" %}

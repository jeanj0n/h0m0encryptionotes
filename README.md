# Define

> The idea behind a homomorphic encryption is that performing certain operations on the data and then encrypting it, is the same as performing these operations on the encrypted data in the first place.
>
> Suppose you have some encryption function e, some data d, and some function f that you wish to apply on the data. If e is homomorphic, then e(f(d)) = f(e(d)), that is if you first encrypt the data and then apply the function, it will be the same as applying the function on the data and then encrypting the result. This means that if you encrypt the data, apply the function and then decrypt the result, it's as if you only applied the function.
>
> What is this good for? Well, suppose f is a function that you don't have the resources to compute on your home computer, but there's some remote server that can do it for you. So you can just send your data to the server to compute the function for you. But what is the data is sensitive, and you don't want the server to have access to it? Then a homomorphic encryption solves this problem. Instead of sending the data to the server, you encrypt it and send the encrypted data. The server computes the function on the encrypted data and sends you the result, which you can decrypt and get the data after the function has been applied to it.

![](<.gitbook/assets/image (21).png>)

![](<.gitbook/assets/image (11).png>)



{% embed url="https://atos.net/en/lp/cybersecurity-magazine-enter-a-new-cybersecurity-era/the-challenges-of-homomorphic-encryption" %}


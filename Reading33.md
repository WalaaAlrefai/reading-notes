# JSON Web Tokens
## What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?

- JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securing transmitting info between parites as a JSON object. 
## How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?
- The info can be verified and trusted becuase it is digitally signed.
- JWTs can be signed using a secret (with the HMAC algo) or a public/private key pair using RSA or ECDSA.
- Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parites.

## When should you use JSON Web Tokens?

- Authorization: Most common scenario. Once user is logged in, each subsequent request will includ the JWT, allowing the user to access routhes, services and resources that are permitted with that token.
- Information Exchange: JWT are a good way of securely transmitting info between parties. Since JWT c an be signed, you can be sure the senders are who they say they are and also the content hasn't been tampered with.

### What is the JSON Web Token structure?

- JWT consist of three parts separated by ( . )
- Header, Payload and Signature.
- JWT look something like this: xxxx.yyyy.zzzzz

#### Header

- consist of two parts: type of token and signing algo being used, such as HMAC, SHA256 or RSA.

#### Payload

- Payload contains Claims. Claims are statements about an entity (the user) and additional data.
- There are three tyups od claims: registered, public and private claims.
- Registered claims: not mandatory but recommended, iss(issuer), exp(expiration time), sub(subject), aud(audience)
- Public: can be defined at will by those using JWTs. To avoid collisions they shjould be defined in the IANA JSON Web Token Registry or be defined as a URI that contains resitant namespace.
- Private: custom claims created to shre information between parties that agree on using them and are neither registered or public claims.

#### Signature

- to create a signature part you have to take the encoded header, the encoded payload, a secret, the algo specified in the header, and sign that.
- signature is used to verify the message wasn't changed along the way, also verifies the sender of the JWT.

### How do JWTs work?

- when users log in using their credentials, a JWT will be returned.
- Should not keep tokens longer than required.
- whenever user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.

## Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?

### it is not suitable for production environments for several reasons:

- __Not optimized for performance:__ The runserver is single-threaded and not optimized for handling a large number of concurrent requests. It doesn't fully leverage the hardware capabilities of a production server and may struggle to handle high traffic loads efficiently.

- __Lack of security features:__ The runserver does not offer the same security features and protections that production-ready servers should have. It lacks options for HTTPS configuration, fine-grained access control, and other security enhancements necessary to protect the application from potential threats.

- __No process manager or automatic restarts:__ In production, it's essential to have a process manager that can automatically restart the server in case of crashes or memory leaks. The runserver does not have such capabilities.

- __Limited scalability:__ The runserver does not support multi-process or multi-threaded deployment, which limits its scalability when trying to handle a significant number of requests concurrently.

- __No load balancing:__ In production, you usually need load balancing to distribute incoming requests across multiple application instances. The runserver does not provide built-in load balancing capabilities.

## To deploy a Django application in a production environment, it is recommended to use a production-ready web server like:

- __Gunicorn (Green Unicorn):__ Gunicorn is a widely used production server for Django applications. It is designed to work with multiple concurrent requests and can be easily integrated with various web servers like Nginx or Apache using reverse proxy settings.

- __uWSGI:__ Similar to Gunicorn, uWSGI is another production-ready server that can serve Django applications efficiently. It provides extensive configuration options and supports multiple protocols.

- __mod_wsgi:__ If you are using Apache web server, mod_wsgi is a good option. It allows you to run Django applications within Apache, providing good performance and stability.

- __Daphne and ASGI servers:__ If your Django application utilizes asynchronous features and uses the ASGI protocol (for example, with Django Channels), you might consider using Daphne or other ASGI servers like uvicorn or Hypercorn.
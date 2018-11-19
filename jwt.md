# JSON Web tokens
- Used for authnetication.
- Looks like:
> https://www.yoursite.com/private-content/?**token=eyJ0eXAiOiJKV1Qi.eyJrZXkiOi.eUiabuiKv**

- Is divided into three parts: header, payload, signature.

    Header- is an object that describes the token along with hashing algorith used.

    Payload - Payload length is proportional to the amount of data stored in jwt.

    Signature - A signature based on header and payload used to verify if the JWT is valid.


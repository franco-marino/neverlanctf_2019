# Dirty Validate

### Question:

To keep my server from doing a lot of work, I made javascript do the heavy lifting of checking a user's password
https://challenges.neverlanctf.com:1135

### How I solved the challenge


![alt text](https://i.imgur.com/Eex0X7H.png?1)


I started with simple tests like "admin: admin" or "admin: weak". I noticed that the error message was generated every time a letter was written, which made me think that a request was made to the server and I checked the requests made by the page through the developers tool


![alt text](https://i.imgur.com/TBCjwOD.png)

![alt text](https://i.imgur.com/DyrcTFs.png)


get_username.php file allows us to obtain the list of available users. Then I tried to do the same with the password field getting the password in base64 of the respective user. Getting this result:

    JimmyOneShoe
    V3JvbmcgdXNlcg==


    Mr. Clean
    bm90IHRoaXMgb25lIGVpdGhlci4uLg0K


    Dr. Whom
    ZmxhZ3tEMG4ndF83cnVzN19KU30=

With a base64 decoder I got the passwords in plain text thus obtaining the flag: **flag{D0n't_7rus7_JS}**

### Flag 
**flag{D0n't_7rus7_JS}**


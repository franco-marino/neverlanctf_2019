# Binary 1

Question:

A user accidentally installed malware on theri computer and now the user database is unavailable.Can yout recover the data and thr flag?
[Attached file]

How I solved the challenge

I started by analyzing the content with *xxd* obtaining a base64 as the hexadecimal output

    xxd -r -p users_db > dump

Very simply with the command

    base64 -d dump > decoded

I got plain text. it was enough to look for the string "flag {"

    grep "flag{" decoded

And this is the flag:

![alt text](https://i.imgur.com/hDHwZKC.png) 


Everything could be done with a single command

    xxd -r -p users_db | base64 -d | grep "flag{"

## Flag

flag{ENC0D1NG_D4TA_1S_N0T_ENCRY7I0N}

# c base64 mini decoder

```void b64d(const char *i, int *ii, char *o, int *oo, int limit);```

 decodes the buffer i into the buffer o
 
 the initial offset of o may be inferior to the initial offsety of i within the SAME BUFFER (palimpseste).
 This is no problem since the output is linearly 3/4th in size of the input.
 
 the method decodes
 - until a character other than ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/ is found
 - or until a limit is reached

when the method returns, ii and oo are filled with the length base64 and decoded respectively.

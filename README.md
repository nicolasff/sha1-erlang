sha1.erl
=====================

This algorithm was ported from the book *Cryptography: Theory and Practice*, by Douglas Stinson.

Two functions are exported, `sha1:binstring/1` and `sha1:hexstring/1`. These functions take a data string in input and output either a binary or a string of uppercase hexadecimal values:

    1> sha1:binstring("test").
    <<169,74,143,229,204,177,155,166,28,76,8,115,211,
        145,233,135,152,47,187,211>>

    2> sha1:hexstring("test").
    "A94A8FE5CCB19BA61C4C0873D391E987982FBBD3"
The library features two functions to hash files, but they are very slow. Also be aware that although SHA-1 outputs 160 bits, an attack exists using 2^63 operations "only".

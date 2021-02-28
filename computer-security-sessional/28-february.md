There will be 1 offline, 2 online and 1 project in this course.

AES

Rinjdael

w4 = w0 XOR g(w3)
w5 = w1 XOR w4
w6 = w2 XOR w5

Round gets multiplied by two every time.

Addition is done by XOR.

### Tasks

- Key Schedule: [Help](https://en.wikipedia.org/wiki/AES_key_schedule#:~:text=AES%20uses%20a%20key%20schedule,keys%20from%20the%20initial%20key.)
- Encryption
- Decryption

[S-Box](https://en.wikipedia.org/wiki/Rijndael_S-box)

[BitVector](https://engineering.purdue.edu/kak/dist/BitVector-3.4.8.html)

Python Code

Row Shifting  
Mix Column

SubBytes, Inverse SubBytes

Encryption: Column Major, swapping in row, left shift, cylindrical

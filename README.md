# RSA-Operations

You are provided with a C++ RSA library. You can extract the required files from the given Zip file.
 
The programs compile and run on Linux/Unix systems. Please use 32 bit systems, or 32 bit flags.
 
Instructions on how to compile and run are given in the myReadme file and samplerun.txt file inside the zip folder. It is preferred that you attempt to solve this problem in a Linux environment, as it is easier for the TA to use one machine to check your programs. (Note: Please read the code contained, there are limitations on the size of numbers they handle.)

Blind signature is a kind of signature, where the signing authority does not know what is being signed. Blind Signatures are used to implement Anonymous money orders. **You have to implement a blind signature scheme.** The scheme you have to implement is described in wikipedia at the link: http://en.wikipedia.org/wiki/Blind_signature
 
The scheme can be briefly stated as:
1. Alice obtains the public key and Modulus N of the person (Bob) who is to sign the message
2. Obtain a random number and its inverse with respect to the Modulus [Not phi] of Bob
3. Alice obtains/generates a message to be signed.
4. Alice encrypts the random number with the public key.
5. Alice multiplies this value by the message
6. Alice then takes a modulus over N
7. Alice sends it to Bob
8. Bob simply decrypts the received value with the private key
9. Bob sends it back to Alice
10. Alice then multiplied the received value with the inverse and takes a modulus over N.
11. The value obtained above is the signed message. To obtain the original message from it, again encrypt it with Bob’s Public Key.
 
To implement the sending and receiving, you may use whatever method you choose, you can use files, pipes or just pass it through functions, or through global memory. Ensure that the random number is around 16 bits long for the program to work correctly.
 
Some encryption examples are shown in rsaDriver.cpp and rsatry1.cpp in the zip file.

###mod1

So the challenge description is pretty self explanatory. We get a message that has a set of numbers. What we do now is mod37 with each number in the message and we have to map the remainder to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrote the following code to solve the problem and get the flag.![Screenshot (2)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/c95800dc-175f-490e-882f-555885488d2f)
The flag-'picoCTF{n33d_a_lArg3r_e_d0cd6eae}'

###miniRSA

Looks like we get a cipher text with bunch of random numbers which is encrypted using RSA algorithm and some instructions. The message could be decoded by writing a python solution script, but I choose to use an online decoder. The image below shows the result.![Screenshot (1)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/ed5a5528-a38e-48c8-8198-956495852b82)
The flag-'picoCTF{R0UND_N_R0UND_ADD17EC2}'

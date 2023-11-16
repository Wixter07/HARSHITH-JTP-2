# GDB Baby Step 1

I had the most fun learning reverse engineering and the use of GDB seemed fun so this problem should be easy I guess. So we have to look for the hexadecimal value stored in the eax register. The porblem gives us a `dbugger0_a` file which is executable. I opened the file on gdb and looked for information all the functions. Well GDB disassbembly by default is set to AT&T syntax, I changed it to intel so as it's more familiar and easy to read. Then I disassembled main. The eax register stored the value `0×86342`. 
![Screenshot (19)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/68c4fe06-272d-4e2c-8c94-8f0223745829)

As per the problem, the flag should be closed in decimal so I converted the hexadecimal value to decimal and got the flag.
![Screenshot (20)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/0c2c8be8-1541-4d14-86bd-13284a4133e8)

The flag-`picoCTF{549698}`

# ARMssembly 0

I learnt a bit of Assembly Language but I wasn't able to read ARM Assembly. So I resorted to looking at the solution from [Martin Carlisle](https://www.youtube.com/watch?v=BMvda3d0dt8) learnt how it works. Basically the code was printing the number the larger number `w0`. The flag could be obtained by converting the decimal number to hexadecimal.
![Screenshot (22)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/400275a7-ffce-4d74-ba7a-e99b19a74c49)

The flag-`picoCTF{E5C69CD8}`

# keygenme-py

So looking at the python file, It is likely that if the key check trial return true, it will lead us to the flag. We already have a portion of the flag and the last 8 characters in it are to be found. The key can be reverse engineered from the check_key function and the below code can give us the the last 8 characters of the flag.
![Screenshot (18)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/251a7b19-9756-46e4-b179-c062fb71be4c)

The flag- `picoCTF{1n_7h3_|<3y_of_e584b363}`



###tunn3l v1s10n

I opened the file on hexed.it website. The header states that it's a Bitmap file. So I changed the file extension to '.bmp' and tried opening it but it gave and error stating that the file format is no supported. So it seems the file has been corrupted. We can compare the file in hand with the acutal bmp file format. I reffered to the bmp size format on Wikipedia and compared the hex values. The hex values  in the header have been replaced with some letters as (BA D0). I didn't know how to  go beyond this point so I had to look up for the solution. I watched a video from Martin Carlisle where he epxlains what hex values can be used to correct the file. After making the corrections, I opened the .bmp file and the image said "notflag{sorry}". So had to go back to the video again to learn that the bmp height size is small. Upon increase the value of it, I got the flag. Images below show the corrected hex values and the flag.![Screenshot (11)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/3e5f8344-a66d-4550-b7f2-bc7ffb4e0d16)

![Screenshot (10)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/74fc29e6-cf3c-4a52-84d7-38abe18a5970)
The flag-'picoCTF{qu1t3_a_v13w_2020}'

###Trivial Flag Transfer Protocol

So TFTP is a simple protocol for exchanging files between to IP machines. I opened the file on wireshark and exported the TFTP object list. I saved the files present in it on my PC. The instructions.txt had bunch of letters which seems to be encoded in some format. I could think of two basic one being base64 and rot13. On decrypting using an online rot13 decrypter, I got a message saying to check the plan file. The plan file had a bunch of characters which I decrypted using the same rot13 decrypter. It said to check out the photos. It could be possible that some information was hidden in the images as it said in the hints. I tried searching for the flag in an hex editor but that didn't workout. So I looked for ways to hiding information in images and then I came to learn about Steganography. I then had to install steghide command on my wsl through "sudo apt install steghide -y". After I looked for a way to use the steghide command through "man steghide", I tried "steghide extract -sf picture1.bmp". It oppened a (Enter passphrase:) promt. Seems that it requires some password. Ok the plan file sai that it hid it with 'DUEDILIGENCE'. This could possibly be the passphrase. It got "couldn't extract any data" message with the first 2 files but got a flag.txt file which I read out what's stored in it using cat command. I got the flag that way.
![Screenshot (13)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/f6fd2eaa-760a-4b39-8e48-bb5042af8d9a)
The flag-'picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}'

###MacroHard WeakEdge

Got a "Forensics is fun.pptm" file. So I thought of looking for macros in the edit section of the ppt but the ppt wasn't opening. I had to look for some help online. This is where I learn that we can unzip ppts. So I tried to unzip it on Windows but didn't work. So I copied the ppt file into my wsl user directory and unzipped the ppt into a another file using the command "unzip Forensics\ is\ fun.pptm -d macro". Had to be extra careful with the spaces in the file path. The I tried navigating through that file and found some set of characters in the hidden file.
![Screenshot (14)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/5a61700b-52d9-42a4-b668-90f6593d461e)
So the letters seem to be encrypted. Again the two basic encryption methods of base64 and rot13  came to my mind. rot13 decrypted didn't give me anything useful but base64 decrypter did.
![Screenshot (15)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/49227ad9-58f8-4cd1-b1d7-2b8d7d05bff3)

The flag-'picoCTF{D1d_u_kn0w_ppts_r_z1p5}'

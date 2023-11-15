###CaaS

So we get a link and an index.js file which prints the input that's written in the curly braces portion of the URL. The index.js file reveals that it prints whateve's written in the curlybraces, but there's also a $ symbol before the braces which means we can try putting some commands before the braces. So I tried using ls command with a message as "https://caas.mars.picoctf.net/cowsay/afk;ls" to get the below result.![Screenshot (3)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/463d468d-7997-4426-b8b7-25abdcfecb5e)
So as expected, the command lists out the files in the cowsay directory and the flag seems to be stored in the falg.txt folder. So we'll try using cat with the file name as "https://caas.mars.picoctf.net/cowsay/afk; cat falg.txt".
![Screenshot (4)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/b15c6216-8990-4a90-b456-fdf1fda49d92)
The flag-'picoCTF{moooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo0o}' 



###Fobidden paths

It seems that we are in some directory with 3 txt files. The problem states that we can't specify absolute file paths and if we do so we get an error message saying "Not Authorized". I looked up the internet to learn about absolute and relative paths. The files are stored in /usr/share/nginx/html/ . So maybe we can read out the flag.txt file by going back 4 directories. That we can do by entering the command "../../../../flag.txt". 
![Screenshot (7)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/b1e0d9e6-9da4-4d6e-a155-9b6bb7bc185c)
The flag-'picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}'

###Local authority

The page asks for username and password as login credential. Inspecting the page doesn't help but upon inspecting the login failure page, we can see a secure.js file which contains the correct login credential. We use that to get the flag.
![Screenshot (5)](https://github.com/Wixter07/CRYPTONITE-JTP-2/assets/150792650/5f4dea44-3367-4c97-8621-62955bac45dc)
The flag-'picoCTF{j5_15_7r4n5p4r3n7_05df90c8}'

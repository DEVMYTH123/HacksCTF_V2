# Write Up

1. First, we need to unzip the ppt. We can see some suspicious folders like ‘maliciousMacroDetails’ and each of these folders has a macro.vba file.
One of these files contains a different text inside it which is the flag in hex. Other files just contain a string “Not a Flag!”.

![Image](https://github.com/user-attachments/assets/130ab5e6-5e58-4e91-993c-7b7b4eb591ec)

2. We can write a script to find this file from a large number of files using a script that prints the unique strings in each of these files. 

![Image](https://github.com/user-attachments/assets/d43068c1-05d1-40c2-9885-0cbf598ed327)

This is the output.

![Image](https://github.com/user-attachments/assets/2bf36778-54be-46da-b25e-cf39dd96e65c)

3. We can decode the hex data to get the flag.

![Image](https://github.com/user-attachments/assets/f4ba5746-661f-4da3-aae6-6397d07ca61f)


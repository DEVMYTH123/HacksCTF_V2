# Write Up

1. Now, The file is a .docx file. Opening it you would see 4 images. One of these images has the flag. You need to extract these files.

![Image](https://github.com/user-attachments/assets/bbe8d256-ce36-4ec9-b6ca-ff2a33eefdfb)

2. First distraction, LSB Steganography has been used on all the four images. But none contains the flag in this form.

![Image](https://github.com/user-attachments/assets/bee6bb40-47d1-4b39-80f5-8838e9e4cb10)

3. The metadata of all the images has also been altered. 3 images just contain useless (useless here means not the flag) information. One of the images has the tag artist in metadata as a bunch of whitespaces.

![Image](https://github.com/user-attachments/assets/3ffe7a95-d2a5-4c35-ae3f-3a6aa5b05758)

4. All whitespaces are not the same. Here two different whitespaces have been used. The artist field contains regular spaces (20) as well as em-spaces (e2 80 83). This can be seen by using a hex editor.

![Image](https://github.com/user-attachments/assets/3b772aa5-7c77-465e-87b6-283199f35577)

5. So, we can create a python script to use ‘0’ or ‘1’ for the em-spaces and the complement for normal spaces. 

![Image](https://github.com/user-attachments/assets/c65ffe4c-c22f-4265-b7d5-ff09df9f665b)

6. Then we can use cyberchef and convert from binary to ascii. This will result in the flag.

![Image](https://github.com/user-attachments/assets/64016282-fa0b-43ed-99da-d4748de7a7a8)

7. It might happen that you will need to flip the binary digits but that just makes the problem tougher.

That’s it. You got the flag: hacks{st3gn0}

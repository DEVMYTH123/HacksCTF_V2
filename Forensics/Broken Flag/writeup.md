# Write Up

1. Let’s first unzip the file

![Image](https://github.com/user-attachments/assets/b438d5e2-4c46-4d89-b0ad-ebd93640e0e8)

2. It contains three png images. Let’s open notFunny.png.

![Image](https://github.com/user-attachments/assets/4c168b15-1ff4-4494-be01-c5e68862a39c)

3. Now, we can do this either manually or using a script. By assigning black pixels to 0 and white pixels to 1.

![Image](https://github.com/user-attachments/assets/b5ab011a-0f9f-4ea7-bf1a-30f0fbba3afd)
![Image](https://github.com/user-attachments/assets/aa0cf6c7-2f48-450f-8bde-06a84bcab834)

4. The output of this script is:

![Image](https://github.com/user-attachments/assets/ede972b6-eb9a-4436-9b03-0ffc164277c3)

5. Copying this to cyberchef, and using “From binary” we get the first part of the flag.

![Image](https://github.com/user-attachments/assets/28d1cb43-1081-4416-bf9d-c85155e90715)

6. For the second part of the flag:
We need to use zsteg on both the images. One will give the value of e, p and q for the rsa algorithm. And the other will give the ciphertext.

![Image](https://github.com/user-attachments/assets/323d7a27-02f7-462a-b386-18de34b0a8e5)
![Image](https://github.com/user-attachments/assets/80695346-134a-490f-b775-3d227f6a320b)

7. Using a script to decrypt the CipherText

![Image](https://github.com/user-attachments/assets/698f55ac-00e4-455a-8450-0018d405ac44)
![Image](https://github.com/user-attachments/assets/8050df00-791f-4548-b2c6-f1bbd49f8b3e)

8. Gives output: Decrypted plaintext message: _rs4_sUcKs}

Combining the flag gives: hacks{im4g3_4nd_rs4_sUcKs}

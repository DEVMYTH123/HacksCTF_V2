# Write Up

1. We start by analyzing the PCAP file in Wireshark. By scrolling through the captured packets, we find that packet numbers 125 and 440 contain JPEG JFIF image files, as indicated in the Info column.

![Image](https://github.com/user-attachments/assets/68dad6ab-9447-41b3-985f-d0ecd0026bdb)
![Image](https://github.com/user-attachments/assets/44c5819d-4c5e-4f6f-90b9-4ff5b813dfcf)

2. To extract the images, we use the following steps:
 - Click on File in the top menu.
 - Navigate to Export Objects > HTTP.

![Image](https://github.com/user-attachments/assets/aed82738-21cd-40f1-a5fd-d4f358c1f1a3)

3.   A new window appears showing a list of HTTP objects. We identify the image files from   packet 125 and packet 440.
 - Select both image files.
 - Click Save All to export them.

![Image](https://github.com/user-attachments/assets/85d37ccd-6e4f-4d83-a5ee-5bc15bf8a679)

4. Now, we can open the saved image files to check their contents.

![Image](https://github.com/user-attachments/assets/61ae44bf-ae46-4175-86bf-a2dfe6cc3197)
![Image](https://github.com/user-attachments/assets/bf680f41-a7e0-4a3c-a955-e66705bf4436)

Flag - hacks{sh4rk_b1t3$_p4ck37$}

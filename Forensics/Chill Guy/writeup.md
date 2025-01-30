# Write Up

In the given challenge, we were provided with a tar archive. Upon extracting it, we found a folder containing two files: file.txt and randomfile.
Running the file command on randomfile, we identified it as a data file. Checking file.txt, it appeared to be a wordlist of some sort. After some attempts, we ran the tail command on file.txt and observed the following output:

ffd8 ffe0 0010 4a46

This looked like a hexadecimal sequence. Suspecting it to be a magic number, we verified the randomfile and replaced its magic number with the given hex code using xxd.
After modifying the file, we ran the file command again and confirmed that the file was now recognized as a .jpeg image. Renaming it accordingly, we opened the image and found a flag—only to realize it was a dummy flag.
Frustrated, we decided to check for hidden data using steghide info, which returned positive results but indicated that the file was password-protected. We then attempted brute-forcing the password using the given wordlist with the stegcracker tool. This revealed that the password was blacksmith.
After extracting the embedded file, the task became straightforward. Finally, we submitted the correct flag:
Hacks{4re_y0u_4_ch1ll_guy}.

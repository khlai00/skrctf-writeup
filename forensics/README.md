# Writeups For Forensic Challenges

## File Signature
Kuki send me a weird file that has no file extensions, can you figure what file is this??

> file

The file has no extensions. Lets try using the `file` command in linux to see what file it is.

![image](https://user-images.githubusercontent.com/57955404/136776140-70fedb2d-d570-498a-bffa-d49f3b7e726d.png)

It turns out it is a JPEG image. View it to get the flag.

## File Signature 2
My friend said that the previous flag is not the real message! Is this file the one that reveals the truth?

> file 

It is hinting that there is another flag hidden in the previous file.

Lets try to find more information on the file. Use `strings` command to see whether if there is any hidden strings in the file.

![image](https://user-images.githubusercontent.com/57955404/136815175-f384a071-9a40-4a58-9542-f0d6a3b83c8c.png)

It seems that there is something called **secret_msg** hidden within the file.

Lets try to unzip it.

![image](https://user-images.githubusercontent.com/57955404/136815706-c5091890-477e-4193-bad2-f1762a396a6a.png)

Unzipping it requires a password. It seems like we are on the right track.

I took a wild guess and input **"skr"** as the password and it works!

The hidden file has been extracted, open it to get the flag.




## Shark Of Wire
OMG! I lost all my network history data, luckily I got capture some data on a pcap file, maybe the flag is inside the file.

> network_data.pcap



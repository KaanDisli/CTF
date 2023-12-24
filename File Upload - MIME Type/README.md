

MIME-type
link to the challenge on RootMe: https://www.root-me.org/en/Challenges/Web-Server/File-upload-MIME-type?lang=en


![resim](https://github.com/KaanDisli/CTF/assets/96348553/311df50e-5c94-4de9-9e1c-beef7336ae78)

We have access to a photo gallery that allows us to upload images of type .jpg .gif and .png
Our goal is to achieve RME by uploading a php file and reading the content of the .passwd file to get the flag


First I uploaded a random image to see how it works

![resim](https://github.com/KaanDisli/CTF/assets/96348553/099d6969-2a4c-410a-905d-79304a0a6bf2)
![resim](https://github.com/KaanDisli/CTF/assets/96348553/70c8ebf5-bbfd-4cfe-878a-2fd2fe00c995)

Once uploaded the server loads the image for you to view in the upload menu

Now we open  Burp Suite to upload a php file, we must keep ' Content-Type:image/jpeg ' to bypass the filter

![resim](https://github.com/KaanDisli/CTF/assets/96348553/736b8a34-83ed-48e4-842a-e5a775d205fa)

this is what I tried first but there is no file named .passwd in the current directory. We have to move up 3 directories but the file is hidden so we use ls -a instead
![c2255c3adfd4e228be0415e6ecf396e6](https://github.com/KaanDisli/CTF/assets/96348553/9c49862d-e337-4903-b2b1-60e0bce2bdcc)



so the final code is:


![720e72c8ff17b3bec3421d8323747a31](https://github.com/KaanDisli/CTF/assets/96348553/ea781cac-ed20-4afc-b392-b0b2a525f84a)



the flag: a7n4nizpgQgnPERy89uanf6T4 

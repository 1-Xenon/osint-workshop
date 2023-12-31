# Find Jerry!
We will now embark on an exciting adventure inspired by the classic rivalry between Tom and Jerry. 
Today, Tom is determined to capture Jerry, who has gone into hiding, making it a challenging task for Tom to find him. But fear not, because your OSINT skills will come to the rescue! 
We have found that Jerry might be hiding inside Tom's Instagram, @tom_the_ct. Your role? To find out where Jerry is hiding and capture him!

# Prerequisites
Install steghide on Kali Linux with the following command: 

```bash
apt install steghide
```

# Solution
1. Head to Instagram and open up Tom's profile at www.instagram.com/tom_the_ct/
2. Upon scrolling through the posts, we find the following links:
   - www.tinyurl.com/answerforfree
   - www.tinyurl.com/iwantfoodpics
   - www.tinyurl.com/getpoorwithme
   - www.tinyurl.com/lolthisisalink
3. We also found that Jerry learnt something new called Base64 (might be useful)
4. Going through the links, we found that www.tinyurl.com/iwantfoodpics is the correct link which will lead you to a Google Drive (https://drive.google.com/drive/u/0/folders/1bC6sRqkU9plypp6z9rcVIZUUm6l6_TXs)
5. After opening a file.txt, we see that there are data that are encoded in a mysterious encoding method. However, we had found that Jerry had learnt Base64 and thus deduced that the data is encoded in Base64.
6. Upon decoding the data, we discovered the following:
   - flandersleftear
   - flanderslefteye
   - iloveehip
   - flandersrightear
   - flandersrighteye
   - eugenerighteye
   - ihateehip
7. With the following data and the bg.jpg file, it can be deduced that the data are passwords that could uncover the data that is hiding behind the picture
8. Download the image and head to Kali Linux to use steghide, the correct password is flandersrightear
9. In Kali, running the following command will allow you to get the file that is hidden:

```bash
steghide extract -sf bg.jpg -p flandersrightear
```
10. A text file will then be received which will contain the flag and a second task
```bash
OSINT{j3rRy_tHe_m0use}
```
```bash
Bonus Challenge:
After capturing Jerry, both of them decided to hide from the owner of the house in one of the rooms, can you look around the house and find them?

Link to house: https://drive.google.com/drive/folders/1tgk0Vm6C166SCCUYH9SAf_6ucy-PbeF3
```
11. Inside the house(https://drive.google.com/drive/folders/1tgk0Vm6C166SCCUYH9SAf_6ucy-PbeF3), there are multiple folders and a text file for us to read. Inside the text file, it tells us to take everything we have seen into consideration.
12. For the second flag, it is hidden in the picture of the Study Room.
13. How to get the password for the second picture? There are 2 ways for you to do so:
    1. Through Jerry's instagram story where the location is shown (deduction)
    2. Through the hint given inside the Toilet folder where it says the password is the country of the picture.jpg file

Password is venezuela (the name of the place inside the picture)
```bash
steghide extract -sf picture.jpg -p venezuela

OSINT{t0m_a&d_j3rRy}
```


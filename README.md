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
3. We also found that Tom learnt something new called Base64 (might be useful)
4. Going through the links, we found that www.tinyurl.com/iwantfoodpics is the correct link which will lead you to a Google Drive and in it contains the following:

![image](https://github.com/1-Xenon/osint-workshop/assets/110148117/17bef071-f8de-43e4-918c-a41fb90ce335)



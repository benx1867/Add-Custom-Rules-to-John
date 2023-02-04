# Add Custom Rules to John
For the ones who can't find how

Feel free to send me custom rules so i can add them to the repository

# Create a rules.conf File in the /usr/share/john Directory
(Change rule to your preferred name):

sudo nano /usr/share/john/rule.conf   


# Add the rules you want in the file
(Change Example-Rule to the rule name you want):

[List.Rules:Example-Rule] 
  
Az"[0-9][0-9]" ^[!@#$]

# Point the rules file in john.conf
sudo nano /etc/john/john.conf

  .include <rule.conf>  
  
 (Leave the < > and . characters and change rule to the name you gave the .conf file)
  
  
 # Use the rule
  john --wordlist=list.lst --rules=Example-Rule hash.txt
  
  (Use the name you gave it in the rule.conf file)

To add multiple rule-sets in single rule.conf file, check: example.conf

The example.conf file has content stolen from here 

https://www.akimbocore.com/article/custom-rules-for-john-the-ripper/

For more information you can check it out.

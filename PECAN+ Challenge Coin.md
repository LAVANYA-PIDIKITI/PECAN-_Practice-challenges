# PECAN+ Challenge Coin
Difficulty:  Intermediate
In 2022 we introduced a challenge coin as a gift to all competitors in the PECAN+ CTF competition.
If you can solve the layers of encryption you will find a flag that can be submitted to the 2023 competition.
NB ignore the final decoded message, the code is for PECAN+ 2023!

![image](https://github.com/LAVANYA-PIDIKITI/PECAN-_Practice-challenges/assets/98797256/a043b088-19a3-4ff3-94ba-6bca9774d3cf)
Developed by: Paul Haskell-Dowland

# Solution:
Now the circumference of the coin is two lines and when you read it alternatively you get
```
WH3R3ISTH3T0UC4N 
MD5ANDXORMAYHELP
```
It clearly says MD5 and XOR may help. The middle symbols are decoded using Templaris cipher which say `TRYEVERYOTHER` <br>
Now we MD5 the string WH3R3ISTH3T0UC4N to get `cb85462fccb075994bc51e42278cd7e7` <br>
Now the left out part is taken and given as input . For the key we use the above MD5 hash <br>
text : 89F72F41AB9001F122B63E244BEDBOC7BFEA661DFC8241A36B955B0166C2E3B08AD6017DF4 <br>
key : cb85462fccb075994bc51e42278cd7e7 <br>
![image](https://github.com/LAVANYA-PIDIKITI/PECAN-_Practice-challenges/assets/98797256/17976714-aced-4e5b-a339-df1d5a61c4f0) <br>
Flag : PECAN4WASGR8 <br>

Link : https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')XOR(%7B'option':'Hex','string':'cb85462fccb075994bc51e42278cd7e7'%7D,'Standard',false)&input=ODlGNzJGNDFBQjkwMDFGMTIyQjYzRTI0NEJFREJPQzdCRkVBNjYxREZDODI0MUEzNkI5NTVCMDE2NkMyRTNCMDhBRDYwMTdERjQ


# All your base
Difficulty:  Intermediate <br>
Can you find the access code?
```c
#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include "base64.h"

int main(){
   setbuf(stdout, 0);
   // Intro message dialogue
   printf("Main screen turn on\n");
   sleep(3);
   printf("How are you\n");
   sleep(2);
   printf("All your base are belong to us\n");
   sleep(2);
   printf("Guess the access code or you have no survive to make your time\n");
   sleep(2);
   printf("HA HA HA HA HA\n");
   sleep(3);
   

   // Guess access code
   
   //code: 411Y0UR8453
   //base64: "NDExWTBVUjg0NTM="	
   	
   char guess[13];
   printf("Enter the access code (Hint: You are the l33t!!):  ");
   scanf("%13s", guess);

   char buffer[13];
   strncpy(buffer, guess, 13);
   buffer[12] = '\0';    // Manually added null terminator

	
   char* code = base64_decode("NDExWTBVUjg0NTM=");
   

   if (strcmp (buffer, code)==0)
   {
   printf("Correct, your flag is: %s, Please submit flag in it's MD5 format\n", code);	
   }	
   
   else
   {
      printf("Incorrect\n");
   }
   

   return 0;
}
```
Developed by: NotALotus

# Solution:
As you can see in the comments there's a code , so just go ahead and try the same :')) <br>

![image](https://github.com/LAVANYA-PIDIKITI/PECAN-_Practice-challenges/assets/98797256/44be15d6-87bd-4171-ad0f-733659abbf10)

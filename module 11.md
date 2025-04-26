

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
#include<math.h>
int maxim(int a,int b,int c, int d)
{
    return fmax(a,fmax(b,fmax(c,d)));
}
int main()
{
    int a,b,c,d,ans;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    ans=maxim(a,b,c,d);
    printf("%d",ans);
}
```
Output:
![Screenshot 2025-04-26 203054](https://github.com/user-attachments/assets/6b98599a-37ec-4e01-8130-850899d5ccfb)

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void maxim(int a,int b)
{
    int max1=0,max2=0,max3=0,i,j,and1,or1,xor1;
    for(i=1;i<=a;i++)
    {
        for(j=1;j<=a;j++)
        {
            and1=i&j;
            or1=i|j;
            xor1=i^j;
            if(i!=j)
            {
                if(max1<and1 && and1<b)
                {
                    max1=and1;
                }
                if(max2<or1 && or1<b)
                {
                    max2=or1;
                }
                if(max3<xor1 && xor1<b)
                {
                    max3=xor1;
                }
            }
        }
    }
    printf("%d\n%d\n%d\n",max1,max2,max3);
}
int main()
{
    int a,b;
    scanf("%d%d",&a,&b);
    maxim(a,b);
}
```
Output:
![Screenshot 2025-04-26 203205](https://github.com/user-attachments/assets/f423be19-505a-4a58-8377-68ff91b3c1ef)

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
int s[100][1000],c[100]={0};
int main(){
    int n,q,x,y,t;
    scanf("%d %d",&n,&q);
    while(q--){
        scanf("%d",&t);
        t==1? (scanf("%d %d",&x,&y), s[x][c[x]++]=y):
        t==2?(scanf("%d %d",&x,&y),printf("%d\n",s[x][y])):
        (scanf("%d",&x),printf("%d\n",c[x]));
    }
}
```
Output:
![Screenshot 2025-04-26 204708](https://github.com/user-attachments/assets/b0f7c699-dd3e-4917-ba84-719daa2a1aff)


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
int main()
{
    int n,i,arr[200],sum=0;
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
        sum+=arr[i];
    }
    printf("%d",sum);
}
```
Output:
![Screenshot 2025-04-26 204346](https://github.com/user-attachments/assets/221e1491-f87f-4eed-89aa-902b4f464179)

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>

int main() {
    char sentence[1000];
    int i = 0, words = 0, inWord = 0;

    fgets(sentence, sizeof(sentence), stdin);

    while (sentence[i] != '\0') {
        if (sentence[i] != ' ' && sentence[i] != '\n') {
            if (inWord == 0) {
                words++;
                inWord = 1;
            }
        } else {
            inWord = 0;
        }
        i++;
    }

    printf("%d\n", words);

    return 0;
}
```
Output:
![Screenshot 2025-04-26 205456](https://github.com/user-attachments/assets/1c3c7392-a2cd-457f-bcd1-a1c379affb00)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.

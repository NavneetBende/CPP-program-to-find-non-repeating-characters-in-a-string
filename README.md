Finding non repeating characters in a string.
In this article we will learn how to code a C++ program to find non repeating characters in a string. First we will calculate the frequency of each character present in the string as non repeating characters are those that are present in the string only once. To calculate the frequency we will use a for loop that will count how many times every unique character is present in the string. And then we will use another for loop to print those characters that have frequency one as these characters are non repeating.

Java program to check frequency of characters in a string
Algorithm:
Initialize the variables and accept the input.
Initialize a for loop. 
This for loop will calculate the frequency of each character.
Terminate this  for loop at the end of string. 
Print the characters having frequency one using another for loop.
While loop in C
C++ Code for finding non repeating characters in a string
#include <iostream>
using namespace std;
int main()
{
    //Initializing variables.
    char str[100]="prepinsta";
    int i;
    int freq[256] = {0};
    
    //Calculating frequency of each character.
    for(i = 0; str[i] != '\0'; i++)
    {
        freq[str[i]]++;
    }
    cout<<"The non repeating characters are: ";
    for(i = 0; i < 256; i++)
    {
        if(freq[i] == 1)//Finding non repeating charcters and printing them.
        {
           cout<<char(i)<<"  " ;
        }
    }
    return 0;
}
Output
Enter the string: prepinsta
The non repeating characters are: a  e  i  n  r  s  t 

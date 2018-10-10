


// Program: anagram
// Purpose: The anagram and non anagram between two strings
// Author:  OMAR SAMY SALEH
// ID:20170176
// Date:    24 Sep 2018

#include <iostream>
// we use this library to be able to enter a string
#include<string>
//we use this library to be able to use sort function
#include<algorithm>

using namespace std;
//boolean function take two strings A and B to check if the two stings is  anagram or not
bool Anagram(string A , string B)
{
int n1 , n2 , i;
//The length of string A is first
n1=A.length();
//The length of string B is second
n2=B.length();

if(n1!=n2)
    return false;
//Function sort to take all letters of the string from begin to end
sort(A.begin(),A.end());
sort (B.begin(), B.end());
for(i=0 ; i<n1 ; i++)
{
//if String A not equal string B therefor it's not anagram
    if(A[i]!=B[i])
    return false;
}
//if String A equal string B therefor it's anagram
 return true;
}
void formUppercaseToLowercase(string& n){
for (int i=0 ; i<n.size(); i++){
    if (n[i]>=65 && n[i] <=90)
    n[i]=(char)(((int)n[i])+32);
}
}
 int main ()
{
string n1,n2;
cout<<"Enter the first word"<<endl;
getline(cin,n1);
cout<<"Enter the second word"<<endl;
getline(cin,n2);
//print out the result by calling anagram function
formUppercaseToLowercase(n1);
formUppercaseToLowercase(n2);
cout<<Anagram(n1,n2);

return 0;
}




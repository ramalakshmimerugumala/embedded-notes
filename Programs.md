## 1. check wheather the number is divisible by 3 or 5 but not both
```
#include <stdio.h>
int main(){
int num;
printf("Enter a number:\n");
scanf("%d",&num);
if((num%3==0||num%5==0)&&num%15!=0){
        printf("It is divisible by 3 or 5 but not both");

}
else{
        printf("The numebr is either divisible by both or neither");
}
}

Output
Enter a number:
3
It is divisible by 3 or 5 but not both
```
## 2.Check wheather the entered character is alphabet or not using logical operator
```
#include <stdio.h>
int main(){
char ch;
printf("Enter a character:");
scanf("%c",&ch);
if(ch=='A'||ch >='Z'||ch=='a'||ch >='z'){
        printf("It is an alphabet");
}
else{
        printf("It is not an alphabet");
}
}
output
Enter a character:#
It is not an alphabet
```
## 3. Write the program to count the no of words in a string
```
#include <stdio.h>
int main(){
char str[100];
int i=0;
int wordcount=0;
printf("Enter a string ");
fgets(str,sizeof(str),stdin);
while(str[i]!='\0'){
        if((str[i]!=' '&&str[i]!='\n')&&
         (str[i+1]==' ' ||str[i+1]=='\n'||str[i+1]=='\0')){
        wordcount++;
        }
i++;
}
printf("No.of words in a  string %d",wordcount);
}
output
Enter a string moon sun
No.of words in a  string 2
``` 
## 4 Count the no of digits in a number
```
#include <stdio.h>
int main(){
        int num;
        int rem=0;
        int count=0;
    printf("Enter the number");
    scanf("%d",&num);
    while(num>0){
            int digit=num%10;
            int rem=rem+digit;
            num=num/10;
            count ++;
    }
    printf("Count the no of digits in a given number %d",count);
}
output
Enter the number345
Count the no of digits in a given number 3
```
## 5 reverse order with difference 2
```
#include <stdio.h>
int main(){
for(int i=10;i>=1;i=i-2){
        printf("%d ",i);
}
}
output
10 8 6 4 2 
```
## 6 sum of the terms
```
#include<stdio.h>
int main(){
        int n,sum=0;
        int term=1;
        printf("Enter the term");
        scanf("%d",&n);
        for(int i=0;i<n;i++){
           sum=sum+term;
           term=term+i;
        }
        printf("%d ",sum);
}
output
Enter the term5
15 
```
## 7 sum of the digits upto single term
```
#include <stdio.h>
int main(){
int number;
    int sum=0;
    int var;
printf("Enter a number");
scanf("%d",&number);
var=number;
while(number>0){
        int digit=number%10;
         sum=sum+digit;
        number=number/10;
}
printf("Sum of the digits in a number is %d",sum);
while(sum>10){
number=sum;
        sum=0;
        while(number>0){
                int digit=number%10;
                sum=sum+digit;
                number=number/10;
        }
}
printf("\nFinal single digit %d\n",sum);
}
output
enter a number 12345
final single digit 6
```
##  Program to get difference of two dates in years, months, days*/
```
#include <stdio.h>
int main(){
int d1,m1,y1;
int d2,m2,y2;
int daysInMonth[]={31,28,31,30,31,30,31,31,30,31,30,31};
printf("enter date1(dd mm yyyy)");
scanf("%d%d%d",&d1,&m1,&y1);
printf("Enter date2(dd mm yyyy)");
scanf("%d%d%d",&d2,&m2,&y2);
if(d2<d1){
        m2=m2-1;
        d2=d2+daysInMonth[(m2-1+12)%12];
}
if(m2<m1){
        y2=y2-1;
        m2=m2+12;
}
int diff_days=d2-d1;
int diff_months=m2-m1;
int diff_years=y2-y1;
printf("difference in days %d",diff_days);
printf("differences in months %d",diff_months);
printf("differences in years %d",diff_years);
}
 output
enter date1(dd mm yyyy)28 02 2020
Enter date2(dd mm yyyy)2 3 2023
difference in days 2
differences in months 0
differences in years 3
```
##   Program to find out the number of notes required for a given amount of money*/ 
```
#include <stdio.h>
int main(){
        int n,choice,notes;
        printf("Enter the amount");
        scanf("%d",&n);
        printf("Enter the value of notes which u begin from");
        scanf("%d",&choice);
        switch(choice){
                case 100:
                   notes=n/100;
                printf("Number of 100 rupess notes required %d\n",notes);
                n=n%100;
               case 50:
                notes=n/50;
                printf("Number of 50 rupess notes are requires %d\n",notes);
                n=n%50;
               case 20:
                notes=n/20;
                printf("Number of 20 rupess notes are required %d\n",notes);
                n=n%20;
               case 10:
                notes=n/10;
                printf("Number of 10 rupess notes required %d\n",notes);
                n=n%10;
               case 5:
                notes=n/5;
                printf("Number of 5 rupees notes are requires %d\n",notes);
                n=n%5;
               case 2:
                notes=n/2;
                printf("Number of 2 rupess notes are required %d\n",notes);
                n=n%2;
           case 1:
                notes=n/1;
                printf("Number of 1 rupee notes are requires %d\n",notes);
                n=n%1;
                break;
               default:
                printf("Enter valid value");
                break;
        }
        printf("\n");
}
output
Enter the amount748
Enter the value of notes which u begin from50
Number of 50 rupess notes are requires 14
Number of 20 rupess notes are required 2
Number of 10 rupess notes required 0
Number of 5 rupees notes are requires 1
Number of 2 rupess notes are required 1
Number of 1 rupee notes are requires 1
```
## Write a program to print all prime numbers from 1 to 99.
```
#include <stdio.h>
int main(){
        int n;
        printf("Enter a number");
        scanf("%d",&n);
        for(int n=2;n<=99;n++){
                int isprime=1;
        for(int i=2;i*i<=n;i++){
                if(n%i==0){
                    isprime=0;
                }
        }
         if(isprime){

                        printf("%d ",n);
        }
}
output
Enter a number1
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 53 59 61 67 71 73 79 83 89 97
```
## 

                                              



//remove duplicate in array


#include <stdio.h>
 
int main()
{
	int arr[10], i, j, k, Size;
	
	printf("\n Please Enter Number of elements in an array  :   ");
	scanf("%d", &Size);
	
	printf("\n Please Enter %d elements of an Array \n", Size);
	for (i = 0; i < Size; i++)
	{
    	scanf("%d", &arr[i]);
   	}     
 
	for (i = 0; i < Size; i++)
	{
		for(j = i + 1; j < Size; j++)
		{
    		if(arr[i] == arr[j])
    		{
    			for(k = j; k < Size; k++)
    			{
    				arr[k] = arr[k + 1];
				}
				Size--;
				j--;
			}
		}
	}

 	printf("\n Final Array after Deleteing Duplicate Array Elements is:\n");
 	for (i = 0; i < Size; i++)
  	{
 		printf("%d\t", arr[i]);
  	}	     
 	return 0;
}




2)) factorial


#include <stdio.h>
int main() {
    int n, i;
    unsigned long long fact = 1;
    printf("Enter an integer: ");
    scanf("%d", &n);

    // shows error if the user enters a negative integer
    if (n < 0)
        printf("Error! Factorial of a negative number doesn't exist.");
    else {
        for (i = 1; i <= n; ++i) {
            fact *= i;
        }
        printf("Factorial of %d = %llu", n, fact);
    }

    return 0;
}


3) total no.of upper and lower cases


#include<stdio.h>

int main()
{
char ch;
int upper=0;
int lower=0;
int digits=0;

while (ch!='*')

{
printf("\nEnter any character, or * to quit :");
scanf("%c",&ch);
ch=getchar();

if (ch>='a'&& ch<='z')

lower++;

if (ch>='A'&&ch<='Z')

upper++;

if (ch>=0)

digits++;

}

printf("\nOutput:");

printf("\nTotal count of lowercase characters entered = %d",lower);

printf("\nTotal count of uppercase characters entered = %d",upper);

printf("\nTotal count of digits entered = %d",digits);


return 0;
}

----------------------------------
Lab sessions

1)
include <stdio.h>

int main()
{
    int num1, num2;
    int sum, sub, mult, mod;
    float div;

    /*
     * Input two numbers from user
     */
    printf("Enter any two numbers: ");
    scanf("%d%d", &num1, &num2);

    /*
     * Perform all arithmetic operations
     */ 
    sum = num1 + num2;
    sub = num1 - num2;
    mult = num1 * num2;
    div = (float)num1 / num2;
    mod = num1 % num2;

    /*
     * Print result of all arithmetic operations
     */
    printf("SUM = %d\n", sum);
    printf("DIFFERENCE = %d\n", sub);
    printf("PRODUCT = %d\n", mult);
    printf("QUOTIENT = %f\n", div);
    printf("MODULUS = %d", mod);

    return 0; 
}
---------------------------------------
2)#include <stdio.h>

int main(){

    int Num, rev_Num = 0, remainder;

    printf("Enter the number to reverse: ");

    scanf("%d", &Num);    

    while (Num != 0){

        remainder = Num % 10;

        rev_Num = rev_Num * 10 + remainder;

        Num = Num/10;

    }    

    printf("The reversed number is: %d", rev_Num);

    return 0;


---------------------------------------
3)#include <stdio.h>
void main(){
  int i,f=1,num;

  printf("Input the number : ");
  scanf("%d",&num);

  for(i=1;i<=num;i++)
      f=f*i;

  printf("The Factorial of %d is: %d\n",num,f);
}
-----------------------------_----------
4)# include <stdio.h>   

int main()   
{   
 int i, Number, Sum = 0 ;   
  
 printf("\n Please Enter any number \n") ;   
 scanf("%d", &Number) ;   
 
 for(i = 1 ; i < Number ; i++)   
  {   
   if(Number % i == 0)   
     Sum = Sum + i ;   
  }    

 if (Sum == Number)   
    printf("\n %d is a Perfect Number", Number) ;   
 else   
    printf("\n%d is not the Perfect Number", Number) ;   

return 0 ;   
}

------------------------------------------
5)#include<stdio.h>
int main()
{
	int age;
	printf("enter age:");
	scanf("%d",&age);
	if(age>=18){
	
	printf("eligible to vote");
}
	else{
	
	printf("%d not eligigble ");
	printf("%d years to wait ",18-age);	
}
}
-----------------------------------------
6)#include <stdio.h>
int main() {
    int year;
    printf("Enter year: ");
    scanf("%d", &year);

    if(year % 4 == 0)
        printf("leap year");
    else
        printf("Not a leap year");
    
    return 0;
}
-----------------------------
7)#include <stdio.h>
int main() {
  int n, i;
  printf("Enter a positive number: ");
  scanf("%d", &n);
  for (i = 1; i <= 10; ++i) {
    printf("%d * %d = %d \n", n, i, n * i);
  }
  return 0;
}
-------------------------------
8)nth prime number

#include <stdio.h>
#include<math.h>
int
main ()
{
  int rangenumber, c = 0, num = 2, i, letest = 0;
  printf ("Enter Nth Number\n");
  scanf ("%d", &rangenumber);

  while (c != rangenumber)
    {
      int count = 0;
      for (i = 2; i <= sqrt (num); i++)
 {
   if (num % i == 0)
     {
       count++;
       break;
     }
 }
      if (count == 0)
 {
   c++;
   letest = num;
 }
      num = num + 1;
    }
  printf ("%dth prime number is %d ",rangenumber,letest);
  return 0;
}

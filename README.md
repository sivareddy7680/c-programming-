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



4)

# Computer Programming (CS0.101)
### [Monsoon 2021-22]
---
## Coding Quiz - 1
---

Q. Write a program to find the nth positive integer having "k" unique factors.
_It is guaranteed that the test cases are such that the answer will be a positive integer <= 1e5._
_It is guaranteed that for 2/3rd of the test cases, answer will be a positive integer <= 1e4._

**NOTE** : If you get TLE Verdict on some of the test cases, think of a better solution of how to find the factors of a number.

For eg :
 - 1 has 1 factor.
 - 2 has 2 factors.
 - 3 has 2 factors.
 - 4 has 3 factors.
 - 5 has 2 factors.
 - 6 has 4 factors.
 - 7 has 2 factors.
 - 8 has 4 factors.
 - 9 has 3 factors.

So, the 3rd integer having 2 factors is ``` 5 ```.
So, the 2rd integer having 3 factors is ``` 9 ```.

**Input Format**
The first line will have 2 integers "n" & "k" separated by a single space.

**Constarints**
 - 1 <= n <= 1000.
 - 1 <= k <= 200.
 - Time : 1s
 - Memory : 64 MB.

**Output Format**
Print a single integer as the answer.

**Sample Test Cases**
1. Test Case 1
_INPUT_ ```3 108```
_OUTPUT_ ```70560```

2. Test Case 2
_INPUT_ ```7 8```
_OUTPUT_ ```66```
  
**Sample Code Answer**

1. Code 1

```C
#include <stdio.h>
#include <math.h>

int Factor(int n, int k)
{
    int d = 1;
    while (d * d <= n)
    {
        if (n % d == 0)
        {
            if (--k == 0)
                return d;
        }
        ++d;
    }

    while (--d >= 1)
    {
        if (d * d == n)
            continue;
        if (n % d == 0)
        {
            if (--k == 0)
            {
                return n / d;
            }
        }
        
    }
    return -1;
}

int main()
{
    long int n, k;
    scanf("%ld %ld", &n, &k);
    long int i = 1;
    do
    {
        int a = Factor(i, k);
        if (a == i)
        {
            n -= 1;
        }

        if (n == 0)
        {
            printf("%ld\n", i);
            return 0;
        }
        i++;
    } while (1);

    return 0;
}

```

2. Code 2

```C
//the following code is >100x facter than traditional method, should be on fingertips
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include <math.h>

int main(int argc, char *argv[]) 
{
	int x,k,n;
	x=scanf("%d %d",&n,&k);
	if(x<0)
		{
			return 1;
		}
	int value=0,count=0;
	for(int i=1;i<=100000;i++)
		{
			int factors=0;
			for(int j=1;j<=sqrt(i);j++)
				{
						if(i%j==0)
							{
								if(i/j==j)
									{
										factors++;
									}
								else
									{
										factors+=2;
									}
							}
				}				
			if(factors==k)
				{
					count++;
				}
			if(count==n)
				{
					value=i;
					break;
				}
		}
		printf("%d",value);
}
```
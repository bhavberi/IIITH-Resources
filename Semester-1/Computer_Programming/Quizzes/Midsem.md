# Computer Programming (CS0.101)
### [Monsoon 2021-22]
---
## Mid Semester Examination
---
1.  Suppose that 'a' is one-dimensional array and 'p' is pointer variable. Assuming that the assignment p=a has just been performed, which of the following are illegal because of mismatched type ?
  - [ ] p[0]==a[0]
  - [ ] p=&a[0]
  - [ ] *p==a[0]
  - [x] p==a[0]

2. How many times the function fib is activated or called ?
``` C
    #include <stdio.h>
    int fib(int n)
    {
      if(n<=1)
        return 1;
      return fib(n-1)+fib(n-2);
    }
    int main()
    {
      fib(3);
      return 0;
    }
```

  - [ ] 3
  - [ ] 4
  - [x] 5
  - [ ] 6

3. What is the output of the below program on the keyboard input "12 thirty-two" ?
```C
    #include <stdio.h>
    int main()
    {
    int n1, n2, retval;
    retval=scanf("%d %d",&n1,&n2);
    printf("scanf retval = %d\n",retval);
    return 0;
    }
```
  - [ ] 0
  - [x] 1
  - [ ] 2
  - [ ] -1

4. What will be ouput of the program on the keyboard input "12 32" ?
```C  
  #include <stdio.h>
  int main()
  {
    int n1,n2,retval;
    retval = scanf("%d %d",&n1,&n2);
    printf("scanf retval=%d\n",retval);
    return 0;
  }
```
  - [ ] 0
  - [ ] 1
  - [x] 2
  - [ ] -1

5. How many times the function fib is activated or called ?
```C
#include <stdio.h>
int fib(int n)
{
  if(n<=1)
    return 1;
  return fib(n-1)+fib(n-2);
}
int main()
{
  fib(4);
  return 0;
}
```
  - [ ] 4
  - [ ] 6
  - [x] 9
  - [ ] 10

6.  Pick the correct statement from the below

    1. The best-case time complexity of the bubble sort algorithm without using swap count is n.
    2. The best-case time complexity of the bubble sort algorithm by using swap count is n.
    3. The worst-case time complexity of the bubble sort algorithm without using swap count is n^2.
    4. The worst-case time complexity of the bubble sort algorithm by using swap count is n^2.

  - [ ] Only statements 1,2 and 3
  - [x] Only statements 2,3 and 4
  - [ ] Only statements 1,2 and 4
  - [ ] Only statements 1,3 and 4

7. Which of the following are not legal C identifiers ?

- [x] 1_crore
- [ ] one_crore
- [ ] one_crore_
- [ ] _one_crore

8. What is the return value of printf statement in the below program ?
```C
#include <stdio.h>
int main()
{
  int n=200, retval;
  printf("%d\n",n);
  return 0;
}
```
  - [ ] void
  - [ ] 0
  - [ ] 200
  - [ ] 3
  - [x] 4

9. What is the output of the above program on the keyboad input "12 32.5" ?
```C
#include <stdio.h>
int main()
{
  int n1, n2, retval;
  retval=scanf("%d %d",&n1,&n2);
  printf("scanf retval = %d\n",retval);
  return 0;
}
```
  - [ ] 0
  - [ ] 1
  - [x] 2
  - [ ] -1

10. Consider the followning statements

      1. With respect to space or memory, loop version of factorial is better than the recursive version.
      2. With respect to time, loop version of factorial is better than the recursive version.

    Pick the correct statements from the above

  - [ ] Only statement 1 is correct
  - [ ] Only statement 2 is correct
  - [x] Both the statements are correct
  - [ ] None of the above statements are correct 

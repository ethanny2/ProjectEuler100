


[![Twitter Badge](https://img.shields.io/badge/chat-twitter-blue.svg)](https://twitter.com/ArrayLikeObj)

# Hacktober Fest 2020 Contribution #3

<p align="center">
  <img src="https://i.gyazo.com/e9bb5a694b5d0b47eab8117d94c653d9.png" alt="Demo gif">
</p>

## Concepts/ Tech
- OSS / Team Git collaboration
- C string manipulation
- Memory allocation
- nth Largest Palidrome Problem


## Contriubtions


<p align="center">
  <img src="https://i.gyazo.com/0d9e5678aa8aab30ce091478efa058da.png" alt="Demo gif">
</p>

[Link to the closed issue](https://github.com/yafiwebdev/ProjectEuler100/pull/124)


### Determining if a string is a Palindrome (C)
```
bool isPalindrome(int num){
    //Fits any int 
    char str[12];
    sprintf(str, "%d", num);
    int startIdx = 0; 
    int endIdx = strlen(str) - 1;
    bool retVal = true;
    while(endIdx > startIdx){
        char left = str[startIdx];
        char right = str[endIdx];
        endIdx--;
        startIdx++;
        //Not a palindrome
        if(left != right){
            retVal = false;
            break;
        }
    }
    return retVal;
}

```

### Largest palindrome made from the product of two n-digit numbers
Calculates the largest palindrome made from the product of two n-digit numbers.
 *   n: To how many digits do you want to calculate the palindrome. 
 *   (e.g  n = 2 max is 99 min is 10, n = 3 max is 999 min is 100)

```
int getLargestNthDigitPalindromeProduct(int n){
    // Use n to calculate the nth digit max num and min num
    char* max = (char*)malloc((n+1) * sizeof(char));
    int largestFound = -1;
    int minNum = pow(10,n - 1);
    while(n){
        strcat(max, "9");
        n--;
    }
    const maxNum = atoi(max);
    for (int i = maxNum; i >= minNum; i--){
        for (int j = maxNum; j >= minNum; j--){
            int prod = i * j;
            if( largestFound < prod && isPalindrome(prod)){
                largestFound = prod;
            }
        }
    }
    printf("Largest found palindrome number [%d] for %d digit numbers \n.", largestFound, n);
    return largestFound;
}
```
--------------------------------------------------------------------------------



# Project Euler Problems' Solutions
Introduced by [FreeCodeCamp](https://www.freecodecamp.org/), "ProjectEuler100" is a challenge for solving at least the first 100 algorithm problems on [Project Euler](http://projecteuler.net/)

I love working on algorithms every now and then, and this challenge is a very nice way of doing that, as it has a specific motivating goal.
So, I am really excited to join the others and embark on this journey, powered by great motivation to be a bit better every day.
Why not join us?

## Main Languages Used (by owner)
- JavaScript
- PHP
- Python

## Other Languages (contributors)
- Java
- Go
- Ruby
- C
- C++
- C#
- Scala

## Contributing to this repository
I started this repo for my personal use to document my own solutions, but feel free to contribute and add your solutions in **other** programming languages.

### Why contribute?
It would be a great way to provide solutions in as many programming languages as possible in one single repository as a reference to help others learn more.

### Contribution Rules
- Follow the **file naming convention** used in existing languages' directories
- ***Comment the code*** where necessary to explain to others(or your future forgetful self) why you used certain approaches or methods and what they're exactly doing.

# Big O

> Time Complexity
> Space Complexity

**Ω θ O**
**Ω best case; θ average case; O worst case**

---

**O(n)**

In the following code, n is 10, there are 10 operations in for loop
>Proportional

```java
public static void printItems(int n){
    for(int i = 0; i < n; i++){
        System.out.println(i);
    }
}

```

*O(2n)*

In the following code, passed 10 items and ran 20 times. n+n=2n
No matter what constant, drop the constant（常数）

```java
public static void printItems(int n){
    for(int i = 0; i < n; i++){
        System.out.println(i);
    }
    for(int j = 0; j < n; j++){
        System.out.println(j);
    }
}

```
**O(n^2)**

pass ten and had 100 lines, n*n=n^2
>Loop within a Loop

```java
public static void printItems(int n){
    for(int i = 0; i < n; i++){
        for(int j = 0; j < n; j++){
            System.out.println(i + " " + j);
        }
    }
}

```
>System.out.println(i + " " + j); 
>" "turn whole thing into string

---
---
**Drop Non-Dominant**


```java
public static void printItems(int n){
    for(int i = 0; i < n; i++){
        for(int j = 0; j < n; j++){
            System.out.println(i + " " + j);
        }
    }
    for(int k = 0; k < n; k++){
        System.out.println(k);
    }
}

```
O(n^2)+O(n) = O(n^2+n)
n^2 grow fast, n^2 is dominant term, n is non-dominant, so we drop n, still O(n^2)

---

**O(1)**
**constant time, no matter how many times it has**
>Most effecient 

```java
public static int addItems(int n){
    retrun n + n + n;
}

```
---

**O(logn)**

>very effecient
*将一个数组不断地对半切开，直到找到要找的那个数 Divide and conquer*
*log2^8 = 3*

---
**Different Terms for inputs**

>O(a + b)
```java
public static void printItems(int a, int b){
    for(int i = 0; i < a; i++){
        System.out.println(i);
    }
    for(int j = 0; j < b; j++){
        System.out.println(j);
    }
}

```
In this code, 1st loop run a times, it is O(a); 2rd loop ran b times, it is O(b). 

```java
public static void printItems(int a, int b){
    for(int i = 0; i < a; i++){
        for(int j = 0; j < b; j++){
            System.out.println(i + " " + j);
        }
    }
}

```
>O(a * b)

---
![Github](https://github.com/ziyanw52/Data-Structure_Algorithms/blob/main/Pic/Screen%20Shot%202023-08-12%20at%2012.34.23%20PM.png)

















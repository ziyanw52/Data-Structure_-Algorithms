## Big O

> Time Complexity
> Space Complexity

**Ω θ O**
**Ω best case; θ average case; O worst case**

---

**O(n)**

In the following code, n is 10, there are 10 operations in for loop

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











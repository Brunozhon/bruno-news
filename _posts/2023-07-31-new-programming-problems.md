---
layout: post
title: New Programming Problems
author: Bruno Zhong
excerpt_separator: <!-- more -->
---

Following my knowlege of Java (yes, Java), I have decided to make programming problems.

The problems will be like math problems (like "If Adam has ten apples, and Betty has ten apples, how many apples do they have together"), but you have to program it.

<!-- more -->

## Problem Example

Consider this problem:

> Tom and Tim are painting the border of a rectangle kitchen floor with length `L` and width `W`. If each tile is one unit, how many tiles will they paint.
>
> **Input**
>
> The first and only line will be the values of `L` and `W` separated by a space.
>
> ```
> 10 10
> ```
>
> **Output**
>
> The first line will be the number of squares painted.
>
> ```
> 36
> ```

A Java program to write this could be:

```java
import java.util.Scanner;
import java.util.StringTokenizer;

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    
    StringTokenizer st = new StringTokenizer(sc.nextLine());
    int length = Integer.parseInt(st.nextToken());
    int width = Integer.parseInt(st.nextToken());
    
    System.out.println((length * 2) + ((width - 2) * 2));
  }
}
```

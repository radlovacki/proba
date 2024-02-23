# Збир првих n бројева

## Задатак

Програм у **програмском језику C** који, за унето `n`, израчунава и исписује суму првих `n` бројева.

## Решење

```c
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
int main(void)
{	
	int n, s = 0;
	scanf("%d", &n);
	for(int i = 1; i <= n; i++)
		s += i;
	printf("%d", s);
    return 0;
}
```

## Алгоритам

```mermaid
flowchart TD
    Start --> id1[[int i, n, suma = 0]]
    id1 --> id2[\n/]
    id2 --> id3[suma = 0]
    id3 --> id4{i `<=` n}
    id4 -->|Yes| id40[i = 1 .. n]
    id40 --> id41[suma += i]
    id41 --> id42[i++]
    id42 --> id4
    id4 -->|No| id5[/suma\]
    id5 --> id6[Stop]
```

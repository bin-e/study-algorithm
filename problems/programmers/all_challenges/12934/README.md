---
layout: default
title: 정수 제곱근 판별
parent: Programmers
grand_parent: Problems
nav_order: 12934
---

- Elapsed time: 00:20:00
- Language: Java

<!-- 문제 -->
# 정수 제곱근 판별

[출처](https://programmers.co.kr/learn/courses/30/lessons/12934?language=java)

## 문제 설명

임의의 양의 정수 n에 대해, n이 어떤 양의 정수 x의 제곱인지 아닌지 판단하려 합니다.

n이 양의 정수 x의 제곱이라면 x+1의 제곱을 리턴하고, n이 양의 정수 x의 제곱이 아니라면 -1을 리턴하는 함수를 완성하세요.

## 제한 사항

- n은 1이상, 50000000000000 이하인 양의 정수입니다.

## 입출력 예

| n   | return |
| --- | ------ |
| 121 | 144    |
| 3   | -1     |

## 입출력 예 설명

입출력 예#1

121은 양의 정수 11의 제곱이므로, (11+1)를 제곱한 144를 리턴합니다.

입출력 예#2

3은 양의 정수의 제곱이 아니므로, -1을 리턴합니다.

<!-- 풀이 -->
# 풀이

## Code

``` java
class Solution {
    public long solution(long n) {
        final long MAX = 50000000000000L;
        long answer = -1;

        double sqrt = Math.sqrt(n);
        if( sqrt <= MAX && sqrt >= 1 && (sqrt - (long)sqrt) == 0)
        {
            long i = (long)sqrt;
            answer = (i+1) * (i+1);
        }

        return answer;
    }
}
```

## Commentary

- 일단 Math라이브러리 없이 해결하려 했으나, 삽질이 너무 심해서 일단 가져다 씀
- 생각의 흐름대로 짜긴 했는데, 입력받은 `n`의 제곱근을 구한 것이 MAX 범위 안에 있으면 더해서 `answer`를 만듦
- 단 소수점이 있으면 정수범위가 아니므로 제외
- 큰 어려움은 없었다

## Discussion

- [ ] Math 라이브러리 없이 풀어보고싶긴함

## References
- x
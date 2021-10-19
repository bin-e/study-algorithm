---
layout: default
title: 짝수와 홀수
parent: Programmers
nav_order: 12937
---

- Elapsed time: 00:00:00
- Language: Kotlin

# 짝수와 홀수

[출처](https://programmers.co.kr/learn/courses/30/lessons/12937?language=kotlin)

## 문제 설명

정수 num이 짝수일 경우 "Even"을 반환하고 홀수인 경우 "Odd"를 반환하는 함수, solution을 완성해주세요.

## 제한 사항

- num은 int 범위의 정수입니다.
- 0은 짝수입니다.

## 입출력 예

| num | return |
| --- | ------ |
| 3   | Odd    |
| 4   | Even   |

# 풀이

## Code

``` kotlin
class Solution {
    fun solution(num: Int): String {
        var answer = ""
        
        if(num % 2 ==0) answer = "Even"
        else answer = "Odd"
        
        return answer
    }
}
```

## Commentary

- `정수`범위인데 `자연수`로 착각해서 몇분 삽질했네..
- 간단히 짝수 판별은 2로 나눠서
- 특별한건 없었는데, 원래 `if`문으로 짝수/홀수 일 때 나눠서 `answer`에 넣을까 했는데 어짜피 나눠지면 `0`이고, 나머지는 `1`일테니 배열로 처리
- 나중에 보니까 자연수가 아니라 정수여서 `Math.abs()` 사용해서 절대값으로 만들어서 사용

## Discussion

- [ ] 왠지 절대값을 사용하지 않고 풀어야 문제가 원하는 방향이었을 것 같은데

## References
- x
# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 신지만
- 리뷰어 : 심지안


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  > 정상적으로 동작하였습니다
- [ ] 주석을 보고 작성자의 코드가 이해되었나요?
  > 전체적으로 이해가 잘 되나 메서드가 중첩되어 있는 행에서 각각의 메서드에 대한 설명도 되어있다면 더 이해하기 수월할 것 같습니다.
  > 예를 들어 baglist를 정의한 줄에서 각 함수가 어떻게 작동하는지 작성되어 있다면, 해당 변수를 이해하는데 더 도움이 될 것 같습니다.
- [X] 코드가 에러를 유발할 가능성이 없나요?
  > 실제로 실행하였을 때 에러가 없었습니다.
- [X] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 각 기능마다 상세히 설명되어 있어 제대로 이해한 것 같습니다.
  예를 들어 baglist에 
- [X] 코드가 간결한가요?
  > 목적하는 바에 꼭 필요한 기능들로만 구성되어 있는 것 같습니다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 사칙 연산 계산기
class calculator:
    # 예) init의 역할과 각 매서드의 의미를 서술
    def __init__(self, first, second):
        self.first = first
        self.second = second
    
    # 예) 덧셈과 연산 작동 방식에 대한 서술
    def add(self):
        result = self.first + self.second
        return result

a = float(input('첫번째 값을 입력하세요.')) 
b = float(input('두번째 값을 입력하세요.')) 
c = calculator(a, b)
print('덧셈', c.add()) 
```

# 참고 링크 및 코드 개선
```python
#코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
sorted 함수 정리:https://blockdmask.tistory.com/466
https://bskyvision.com/entry/python-%EB%94%95%EC%85%94%EB%84%88%EB%A6%AC-%EA%B0%9D%EC%B2%B4%EC%9D%98-get-%EB%A9%94%EC%86%8C%EB%93%9C-%EC%82%AC%EC%9A%A9%EB%B2%95
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```

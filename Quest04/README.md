# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 신지만
- 리뷰어 : 심지안


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  > 잘 동작했습니다.
- [ ] 주석을 보고 작성자의 코드가 이해되었나요?
  > 주석이 함수를 만들 때에만 간략히 달려있어서 이해하는데 시간이 걸렸습니다.
  > 예를 들어 show_fish_movement_comprehension() 함수 내의 movement에 할당된 것이 컴프리헨션이고,
  > 그 아래줄부터 해당 컴프리헨션으로 생성된 이터러블 객체를 받아 반복문을 돌림을 명시해주셨으면 이해하는데 더 수월했을 것 같습니다.
  > 
- [X] 코드가 에러를 유발할 가능성이 없나요?
  > 없는 것 같습니다
- [ ] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 각 함수에 맞게 주석이 작성되어 있어 제대로 이해하신 것 같습니다.
- [X] 코드가 간결한가요?
  > 코드가 기능하는 단위에 맞게 쪼개어져 있어서 가독성이 좋다고 생각했습니다
  > 예를 들면 show_fish_movement_comprehension() 함수 내의 show_fish_movement_generator() 함수는인자값을 받아 이터레이터를 생성하고,
  > 그 아래  for m in movement_generator() 그 값을 받아 출력하는데,
  > 함수 내에서도 어떤 기능을 하냐에 따라 또 기능이 분화되어 있어 재활용하기도 좋고 유지관리 하기에도 좋아보였습니다.

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
# 리스트 컴프리헨션 : https://whatisthenext.tistory.com/110

```

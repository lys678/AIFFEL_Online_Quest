# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 신지만
- 리뷰어 : 본인의 이름을 작성하세요.


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [] 주석을 보고 작성자의 코드가 이해되었나요?
  > 위 항목에 대한 근거 작성 필수
- [ ] 코드가 에러를 유발할 가능성이 없나요?
  > 위 항목에 대한 근거 작성 필수
- [ ] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 위 항목에 대한 근거 작성 필수
- [ ] 코드가 간결한가요?
  > 위 항목에 대한 근거 작성 필수

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 미로찾기
from pprint import pprint
'''
start_row: 경로 탐색의 시작 행 인덱스.
start_col: 경로 탐색의 시작 열 인덱스.
end_row: 종료 행 인덱스.
end_col: 종료 컬럼 인덱스.
visited: 행렬에서 방문한 위치를 추적하기 위한 부울 값의 리스트.
path : 탐색 중인 현재 경로를 저장
paths: 찾은 모든 유효한 경로를 저장
'''
def find_path(matrix, start_row, start_col, end_row, end_col, visited, path, paths):
    num_rows = len(matrix) # 리스트 행수
    num_cols = len(matrix[0]) # 리스트 열수

    # 현재 위치가 유효한 리스트 범위인지 이미 방문했지는 판별
    # Check if the current position is out of bounds or already visited

    if (start_row < 0 or start_row >= num_rows or
            start_col < 0 or start_col >= num_cols or
            visited[start_row][start_col] or
            matrix[start_row][start_col] != 0):
        return

    # 현재 위치가 최종 목적지인지 판별
    # Check if the current position is the destination
    if start_row == end_row and start_col == end_col:
        path.append((start_row, start_col))
        paths.append(path[:])  # 해당 경로를 누적 #Add a copy of the path to the paths list
        path.pop()  # Remove the last element from the path
        return

    # 현재 위치를 방문으로 표시
    # Mark the current position as visited
    visited[start_row][start_col] = True

    # 현재 위치를 탐색 경로에 추가
    # Add the current position to the path
    path.append((start_row, start_col))

    # 재귀 방식으로 인접 셀 탐색
    # Explore the neighboring cells in a recursive manner (up, down, left, right)
    find_path(matrix, start_row - 1, start_col, end_row, end_col, visited, path, paths)  # Up
    find_path(matrix, start_row + 1, start_col, end_row, end_col, visited, path, paths)  # Down
    find_path(matrix, start_row, start_col - 1, end_row, end_col, visited, path, paths)  # Left
    find_path(matrix, start_row, start_col + 1, end_row, end_col, visited, path, paths)  # Right

    # 역추적하기 전에 현재 위치를 방문하지 않은 것으로 표시
    # Mark the current position as unvisited before backtracking
    visited[start_row][start_col] = False

    # 역추적하기 전에 경로에서 현재 위치를 제거
    # 알고리즘이 막다른 골목에 도달하거나 목적지로 이어지지 않는 경로를 찾으면 역추적하고 다른 가능한 경로를 탐색해야 합니다.
    # 이 상황에서 path 목록에 추가된 마지막 셀은 유효한 경로의 일부가 아니므로 제거
    # Remove the current position from the path before backtracking
    path.pop()


# Example usage
# 입력 2차원 리스트
matrix = [
    [0, 1, 0, 0, 0],
    [0, 0, 0, 1, 0],
    [0, 1, 1, 0, 0],
    [0, 0, 1, 1, 0],
    [0, 0, 0, 0, 0]
]
start_row = 0
start_col = 0
end_row = 4
end_col = 4
visited = [[False] * len(matrix[0]) for _ in range(len(matrix))]
path = []
paths = []

find_path(matrix, start_row, start_col, end_row, end_col, visited, path, paths)
print('입력된 2차원 리스트 출력')
print('=' * 60)
pprint(matrix, indent=4, width=20)
print('=' * 60)
# Print all the paths
print('유효한 경로 출력')
print('=' * 60)
for p in paths:
    print(p)
print('=' * 60)

import copy
print('리스트에 이동 경로 표시')
print('=' * 60)
#for i in range(2, 3):
for i in range(0, len(paths)):
  print(i + 1,'번째 =>' )
  matrix_tmp = copy.deepcopy(matrix)
  #pprint(matrix_tmp)
#for i in range(0, len(paths)):
  for x, y in paths[i]:
    #print(x, y)
    #matrix_tmp = matrix.copy()
    matrix_tmp[x][y] = '2'
  pprint(matrix_tmp)
  print('*' * 60)
print('=' * 60)
```

# 참고 링크 및 코드 개선
```python
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```

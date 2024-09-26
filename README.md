# 제어문
# 1. 조건문
#  - if
# 2. 반복문
#  - for
#  = while

# 조건문(Condition): if-elif-else
#  - 특정조건을 만족하는 경우 수행할 작업에 사용
#  - 모든 조건은 boolean으로 표현
#  - 조건문의 경우 if, elif, else 블록 내 들여쓰기
#  - 모든 블록문의 시작점은 :(콜론)

# if 조건1:
#     실행문
# elif 조건2:
#     실행문
# elif 조건3:
#     실행문
# else:
#     실행문

# if문 조합식
#  1. if
#  2. if ~ else
#  3. if ~ elif ~ elif
#  4. if ~ elif ~ else

# 2개 이상의 조건을 사용하고 싶은 경우
#  → AND, OR, NOT
#  1. AND : 두 조건이 모두 참인 경우만 참
#  2. OR : 한 조건이라도 참이면 참
#  3. NOT : 참 → 거짓, 거짓 → 참

# 예제) 사용자로부터 출생년도를 입력받고
#       성인, 대, 고, 중, 초, 어린이로 분류하는 코드 자겅하세요.

from datetime import datetime
now = datetime.today().year

# input(): 키보드로부터 값을 입력 받음
#  - 문자열 타입(str)
born = input("출생연도: ")
print(born)
if born > now:
    print(f"{now}보다 작은 출생년도를 입력해주세요.")
    #다시 출생년도 입력 받기
    

#print(type(now))
#print(type(born))

age = now - int(born)
print(age)

# 27이상 성인
# 20~26 대학생
# 17~19 고등학생
# 14~16 중학생
# 8~13 초등학생
# ~7 어린이
if  age>=27:  # False: 26↓
    category = "성인"
elif age>=20:  # False: 19↓
    category = "대학생"
elif age>=17:
    category = "고등학생"
elif age>=14:
    category = "중학생"
elif age>=8:
    category = "초등학생"
elif age>=0:
    category = "어린이"
else:
    print("잘못 입력하셨습니다.")

print(f"출생연도는 {born}, 나이는 {age}로 당신은 {category}입니다.")

# 반복문
#  - for:   반복 횟수를 아는 경우,   예) 게시판
#  - while: 반복 횟수를 모르는 경우, 예) 키오스크

# 반복문(Loop)
#  - 반복적인 작업을 가능하게 해주는 도구
#  - list, str, tuple 등 컬렉션 타입의 아이템을 하나씩 순화하면서 사용(for)
#  - 특정 조건을 만족하는 경우(while)

# JAVA & C for문 문법
#for(int i=0;i<=9;i++){
#    실행문;
#}

# i in range() or 컬렉션
# range() or 컬렉션의 길이만큼 반복
for i in range(10):
    print(i)
    
for i in [1, 2, 3]:
    print(i)
    
# range(시작, 끝, 인터벌) : 범위 값을 만들어 줌
#  - 시작을 생략하면 0부터
#  - 인터벌을 생략하면 1
# range(1, 5)    → 1, 2, 3, 4
# range(1, 5, 2) → 1, 3
# range(7)       → 0, 1, 2, 3, 4, 5, 6

a = ["A", "B", "C"]

# 반복횟수(인덱스)를 알고 싶은 경우 → enumerate()
for i, val in enumerate(a):
    print(val)

# 구구단 2단 출력
# 2x1=2
# 2x2=4
# 2x3=6
# 2x4=8
# 2x5=10
# 2x6=12
# ...
# 2x9=18

for i in range(1, 10):
    print(f"2x{i}={2*i}")
    
# 중첩 for문
for i in 범위:
    for j in 범위:
        for k in 범위:
            
# 숙제: 구구단 2단~9단까지 출력하는 코드 작성(중첩 for문 사용)
#  - 반복1: 구구단 2단~9단
#  - 반복2: 단, 1~9 곱셈
# while
#  - 조건이 참인경우 반복 실행
#  - 조건이 거짓인 경우 반복 중단
#  - 조건을 True(boolean) → 무한 반복
#    (break문과 함께 사용)

#  for, while에서 사용할 수 있는 키워드
#   1. break:    즉시 반복문 종료
#   2. continue: 즉시 다음 반복으로 넘어가기

#while 조건:
#    실행문

while True:
    print("test")
    if True:
        break
    
print("Hello")

# 숙제: for문으로 작성한 구구단 2단을 while문으로 작성해보세요.
for i in range(1, 10):
    print(f"2x{i}={i*2}")

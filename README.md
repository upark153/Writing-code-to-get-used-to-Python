# Writing-code-to-get-used-to-Python
![image](https://user-images.githubusercontent.com/115389450/233533144-86c19af1-b28e-42a5-8444-c67cdee0b303.png)
```
languages = ['python', 'perl', 'c', 'java]
for lang in languages:
     if lang in ['python', 'perl']:
        print("%6s need interpreter" % lang)
     elif lang in ['c', 'java]:
        print("%6s need compiler" % lang)
     else:
        print("should not reach here")
```
```
for a in [1, 2, 3]:
    print(a)
```
```
i=0
while i < 3:
     i = i +1
     print(i)
```
```
def add(c, d):
     return c + d
```
![image](https://user-images.githubusercontent.com/115389450/233533263-fbb9ae1c-b3ff-4884-a23d-454eebe19bae.png)
![image](https://user-images.githubusercontent.com/115389450/233533351-dc701255-9c6e-4abb-be66-8d21ab31dc07.png)
```
print("10진수  2진수  8진수  16진수")
for i in range(1, 11):
    binary = bin(i) # 2진수 변환 함수
    octal = oct(i) # 8진수 변환 함수
    hexa = hex(i) # 16진수 변환 함수
    print(f'{i}       {binary}   {octal}   {hexa}')
```
![image](https://user-images.githubusercontent.com/115389450/233533390-186932e8-f969-4849-9d66-98202cfea45b.png)
![image](https://user-images.githubusercontent.com/115389450/233533438-fbad46df-8208-480e-8d65-389cdc8aca58.png)
![image](https://user-images.githubusercontent.com/115389450/233533480-da711740-5117-438e-a263-b50d41407982.png)



![image](https://user-images.githubusercontent.com/115389450/233532172-d014b55c-3c3a-4748-9418-97dbe680fffa.png)
```
print("아침 7시, 알람소리를 듣고 일어났다.")
print("원래는 8시에 일어났지만, 1시간일찍 알람맞추기 방법으로 매일 7시에 일어나게 되었다")
print("원래 일어난 시간을 입력하면 당신의 하루일과 게임이 시작됩니다.")
h, m = map(int, input("원래일어난 시간을 입력해주세요 : ").split())
m -= 60
if m < 0:
    h -= 1
    m += 60
    if h < 0:
        h = 23
print("일어난 시간:%d, 몇분:%d" %(h, m))
class human():
    def __init__(self):
        self.name =""
        self.hp = 0
        self.exp = 0
        self.lv = 1

    def 밥먹기(self):
        print(self.name,'이(가) 밥을 먹는다. 체력을 회복합니다.')
    def 잠자기(self):
        print(self.name,'이(가) 잠을 잔다. 체력을 회복합니다.')
    def 운동하기(self):
        print(self.name,'이(가) 운동한다. 체력이 감소하고, 경험치가 오릅니다.')
    def 파이썬공부하기(self):
        print(self.name,'이(가) 파이썬을 공부한다. 체력이 감소하고 경험치가 오릅니다.')
    def 레벨체크(self):
        print(self.name,'레벨체크')
    def 상태정보(self):
        print(self.name,'상태정보출력')
        print('HP:', self.hp)
        print('EXP:', self.exp)
        print('LV:', self.lv)

class 박의용(human):
    def __init__(self):
        super().__init__()
        self.name = '박의용'
        self.hp = 100

    def 밥먹기(self):
        super().밥먹기()
        self.hp += 33

    def 잠자기(self):
        super().잠자기()
        self.hp += 42

    def 운동하기(self):
        super().운동하기()
        self.hp -= 33
        start = self.hp>0
        if start:
            self.exp += 10
            self.레벨체크()
        return start
    def 파이썬공부하기(self):
        super().파이썬공부하기()
        self.hp -= 38
        start = self.hp>0
        if start:
            self.exp += 50
            self.레벨체크()
        return start
    def 레벨체크(self):
        if self.exp>=10:
            self.lv += 1
            print(self.name, '레벨업!')
            self. exp -=10
    def 음유시인(self):
        print("방랑자의 부름, 우주의 결속,수호자의 성소 내딛는 곳은 어디든 나의 세상 음. 인생은 짧은 여행이라네")

class 이현도(human):
    def __init__(self):
        super().__init__()
        self.name = '이현도'
        self.hp = 200

    def 밥먹기(self):
        super().밥먹기()
        self.hp += 10

    def 잠자기(self):
        super().잠자기()
        self.hp += 15

    def 운동하기(self):
        super().운동하기()
        self.hp -= 80
        start = self.hp>0
        if start:
            self.exp += 40
            self.레벨체크()
        return start
    def 파이썬공부하기(self):
        super().파이썬공부하기()
        self.hp -= 10
        start = self.hp>0
        if start:
            self.exp += 10
            self.레벨체크()
        return start
    def 레벨체크(self):
        if self.exp>=10:
            self.lv += 1
            print(self.name, '레벨업!')
            self. exp -=10
    def 중국권법(self):
        print("자네 무술을 아시는가? 태극권법의 창시자 내 주먹을 받으면 자넨 사망에 이를것이네 살려면 도망가시게")

class 고연재(human):
    def __init__(self):
        super().__init__()
        self.name = '고연재'
        self.hp = 250

    def 밥먹기(self):
        super().밥먹기()
        self.hp += 30

    def 잠자기(self):
        super().잠자기()
        self.hp += 25

    def 운동하기(self):
        super().운동하기()
        self.hp -= 60
        start = self.hp > 0
        if start:
            self.exp += 40
            self.레벨체크()
        return start
    def 파이썬공부하기(self):
        super().파이썬공부하기()
        self.hp -= 80
        start = self.hp > 0
        if start:
            self.exp += 30
            self.레벨체크()
        return start
    def 레벨체크(self):
        if self.exp>=10:
            self.lv += 1
            print(self.name, '레벨업!')
            self. exp -=10
    def 우사인볼트(self) :
        print("난 이세계 최고 바로 우사인볼트. 난 키가 크기 때문에 스타트 속도는 느리지만 중간지점부터는 끝까지 간다")

class Menu:
    def __init__(self, humanchoice):
        self.humanchoice = humanchoice

    def run(self):
        start = True
        while start:
            menu = int(input('1.밥먹기 2.잠자기 3.운동하기 4.파이썬공부하기 5.상태확인 6.특성발현 7.종료'))
            if menu == 1:
                self.humanchoice.밥먹기()
            elif menu == 2:
                self.humanchoice.잠자기()
            elif menu == 3:
                self.humanchoice.운동하기()
            elif menu == 4:
                self.humanchoice.파이썬공부하기()
            elif menu == 5:
                self.humanchoice.상태정보()
            elif menu == 6:
                if isinstance(self.humanchoice, 박의용):
                    self.humanchoice.음유시인()
                elif isinstance(self.humanchoice, 이현도):
                    self.humanchoice.중국권법()
                elif isinstance(self.humanchoice, 고연재):
                    self.humanchoice.우사인볼트()
            elif menu == 7:
                start = False
        print('하루 일과 종료')
        print('사실 요새 하루일과가...')
        print('일어나서 밥먹고 수업듣고, 다시 밥먹고...')
        print('공부하고...자고..의 반복이라')
        print('약간 재미있게 할 수 없을까 하여..')
        print('혼자서 만들지는 못했지만')
        print('나중에 더 학습하여 더 재밌는 게임을 만들고 싶습니다.')
def main():
    print('하루 일과 게임 시작')
    human = input('사람 선택\n1.박의용(기본)2.이현도 3.고연재')
    humanchoice = None
    if human == '1':
        humanchoice = 박의용()
    if human == '2':
        humanchoice = 이현도()
    if human == '3':
        humanchoice = 고연재()

    humanchoice.상태정보()
    click = Menu(humanchoice)
    click.run()
main()
```

![image](https://user-images.githubusercontent.com/115389450/233532234-0e4c120c-051e-4e86-986c-0a25a4454f2f.png)

[파이참 에디터에서 원하는 문자 바꾸기](https://signing.tistory.com/60)

[알람 프로그램?](https://coding-of-today.tistory.com/147)

[파이썬 map(int(input().split()](https://dojang.io/mod/page/view.php?id=2286)

[파이썬 게임 코드 참조](https://whyjoosokkagi.tistory.com/54)

![image](https://user-images.githubusercontent.com/115389450/233532567-f7203c3b-b7f0-497a-8324-a319923d252e.png)

![image](https://user-images.githubusercontent.com/115389450/233535504-c94bd49b-f282-497f-bb8c-09eabc06b5a4.png)
```
while True:
    money = 10000
    coffee = int(input("안녕하세요 손님 커피를 몇 잔 만들어드릴까요? 커피는 1잔당 5000원입니다.:"))
    coffeetotal = coffee*5000
    if money<coffeetotal:
        print(f'돈이부족합니다. 필요하신돈은 {coffeetotal-money}원입니다. ')
        lessMoney = int(input(f'그렇군요, 돈 더 드리겠습니다. : '))
    print(f"커피를 {coffee}잔 만들어드리겠습니다.")
    i = 0
    while i<=5:
        print(f"커피 제조중입니다. {i}분 지났습니다.")
        i = i + 1
    print(f"요청하신 커피 {coffee}잔 나왔습니다. 즐거운 하루 되세요")
    break
```
![image](https://user-images.githubusercontent.com/115389450/233535572-6751affd-88b6-4bee-b658-84dd0839ad3f.png)
```
uzacha = 1200
coffee = 500
cocoa = 300
money = int(input("음료수를 사기 위해 돈을 넣어주쎄용 : "))
range1 = money//uzacha
range2 = money//coffee
range3 = money//cocoa
for i in range(0, range1+1):
    for j in range(0, range2+1):
        for k in range(0, range3+1):
            sum = i * uzacha + j * coffee + k * cocoa
            if sum>money-300 and sum<=money:
                print(f'유자차{i}개, 커피{j}개, 코코아{k}개를 살 수 있습니다.')
```
```
for i in range(0, 9):
    for j in range(0, 21):
        for k in range(33, 0, -1):
            sum = i * uzacha + j * coffee + k * cocoa
            if sum>=9700 and sum<=10000:
                print(f'유자차{i}개, 커피{j}개, 코코아{k}개를 살 수 있습니다.')
```
```
#유자차 1200원, 커피 500원 코코아 300원
drink = {'uzacha':1200, 'coffee': 500, 'cocoa': 300}

sum = 0
money = int(input("음료수를 사기 위해 돈을 넣어주쎄용 : "))
while True:
    leftMoney = money - sum
    print(f'현재 잔액은{leftMoney} 남았습니다.')
    choice = input("음료수 선택(M), 계산하기(B), 종료(C) : ")
    if choice == 'M':
        drinkchoice = input("원하는 음료를 영어로 입력해 주세요 : ")
        if drinkchoice == 'uzacha':
            sum += drink['uzacha']
            if sum>money:
                print(f"돈이 부족합니다. 잔돈을 {leftMoney}을 반환해드립니다.")
                break
            else:
                print("유자차 1개 나옵니다. 또르륵")
        elif drinkchoice == 'coffee':
            sum += drink['coffee']
            if sum > money:
                print(f"돈이 부족합니다. 잔돈을 {leftMoney}을 반환해드립니다.")
                break
            else:
                print("유자차 1개 나옵니다. 또르륵")
        elif drinkchoice == 'cocoa':
            sum += drink['cocoa']
            if sum > money:
                print(f"돈이 부족합니다. 잔돈을 {leftMoney}을 반환해드립니다.")
                break
            else:
                print("유자차 1개 나옵니다. 또르륵")
            continue
    if choice == 'B':
        print(f'계산합니다. 잔돈은 {leftMoney}입니다.')
        break
    if choice == 'C':
        print("종료합니다.")
        break
```
![image](https://user-images.githubusercontent.com/115389450/233535672-0c3234c5-d0dd-42ee-8afd-53c3acbb3577.png)
```
sum = 0
uzacha = 1200
coffee = 500
cocoa = 300
money = int(input("음료수를 사기 위해 돈을 넣어주쎄용 : "))
range1 = money//uzacha
range2 = money//coffee
range3 = money//cocoa
print(f'유자차 : {range1}개, 커피 : {range2}개, 코코아 : {range3}개 살 수 있습니다.(각각 최대갯수)')
print(f'유자차 : 1200원, 커피 : 500원, 코코아: 300원 입니다.')
while True:
    choice = int(input("유자차 개수를 말씀 해 주세요."))
    choice2 = int(input("커피 개수를 말씀 해 주세요."))
    choice3 = int(input("코코아 개수를 말씀 해 주세요."))
    drinktotal = uzacha*choice + coffee*choice2 + cocoa*choice3
    if drinktotal>money:
        print("돈이 부족해요 다시 선택해주세요,")
    else:
        print(f"총 금액은 {drinktotal}원 입니다.")
        print(f"잔돈 {money-drinktotal}원 남겨 드립니다.")
        break
```
![image](https://user-images.githubusercontent.com/115389450/233535714-fbe122fa-5747-46b1-97a7-45a5c904d3de.png)

![image](https://user-images.githubusercontent.com/115389450/233544647-78e07e2a-8fc5-4b99-8f4c-a755c0701942.png)
```
# string concatenation ( aka how to put strings together )
# suppose we want to create a string that says "sybscrbe to _____"
youtuber = "upark" # some string variable
# a few ways to do this
print("subscribe to " + youtuber)
print("subscribe to {}".format(youtuber))
print(f"subscribe to {youtuber}")
```
```
adj = input("Adjective: ")
verb1 = input("Verb: ")
verb2 = input("Verb: ")
famous_person = input("Famous person: ")
madlib = f"Computer programming is so {adj}! It makes me so excited all the time because \
I love to {verb1}. Stay hydrated and {verb2} like you are {famous_person}!"

print(madlib)
```
```
import random
# 추측게임을 구현하는 방법
# 컴퓨터에는 비밀 번호가 있습니다.
# 그리고 우리는 그 비밀 번호를 추측하려고 노력하고 있습니다.
# 1. 실제로 우리가 추측할 수 있도록 컴퓨터가 비밀번호를 생성하게 하는 것
# 2. 컴퓨터에 임의의 숫자가 있으면 정확하게 추측해야 하며 터미널에서 추측해야 한다.
# 3. 추측한 숫자를 입력하면 컴퓨터가 숫자가 너무 높은지 여부를 알려줍니다.
# 4. 너무 낮은, 또는 숫자를 올바르게 추측 했다면 다음까지 반복해야 한다.
# 5. 반복할 사전 정의된 유니버스가 없다면 , while 루프를 사용할 것이다.
# 6. 숫자는 난수와 같다.
# 7. 추측이 임의의 숫자와 같지 않은 경우 몇 가지를 반복하려고 한다.
# 8. 변수를 초기화하려면 이 변수가 존재한다고 python에 알립니다.

def guess(x):   # x를 매개 변수로 만들어 이 임의의 숫자 가져오기 함수에 전달할 수 있도록 하겠습니다.
    random_number = random.randint(1, x)
    guess = 0 # 임의의 숫자 rand int 1과 x 사이 그리고 그것은 결코 0이 되지 않을 것이라는 것을 의미한다.
    while guess != random_number:
        guess = int(input(f'Guess a number between 1 and {x}'))
        if guess < random_number:
            print('Sorry, guess again. Too low.')
        elif guess > random_number:
            print('Sorry, guess again. Too high.')

    print(f'Yay, congrates. You have guessed the number. {random_number} correctly!!!')
guess(20)  # 함수 호출
```
```
import random
# 반대로 컴퓨터가 추측하려고 한다.
# 컴퓨터 손님이라는 새 기능
# 비밀 번호가 있는데, 어떤 비밀 번호가 맞는지 컴퓨터에 알리지 않겠다.
# 이는 기본적으로 컴퓨터가 최소값과 최대값으로 작업 할 수 있는
# 숫자의 범위를 가지고 있음을 의미한다.
# 낮고 높음. 즉, 초기에 낮은 값과 높은 값을 설정하자는 의미
# 이것은 어떤 것도 반복할 필요가 없다.
# 사용자가 피드백을 제공할 수 있을 때까지
# 컴퓨터에 피드백이 너무 많은지 알려줄 수 있어야 합니다.
# 높거나 너무 낮거나 정확하게 추측한 경우 피드백을 초기화하겠습니다.
# guest를 0으로 초기화하는 것과 마찬가지로
# 빈 문자열로 초기화 해 보겠습니다.
# 컴퓨터가 해야 할 첫 번째 일은 새 번호를 받는 것입니다.
# 그래서 추측을 할 것이다.

def computer_guess(x):
    low = 1
    high = x
    feedback = ''
    while feedback != 'c':
        if low != high:
            guess = random.randint(low, high)
        else:
            guess = low # could also be high b/c low = high
        guess = random.randint(low, high)
        feedback = input(f'Is {guess} too high (H), too low (L), or correct (C)?? ').lower()
        if feedback == 'h':
            high = guess - 1
        if feedback == 'l':
            low = guess + 1

    print(f'Yay ! The computer guessed your number, {guess}, correctly! ')
computer_guess(1000)
```
![image](https://user-images.githubusercontent.com/115389450/233544757-da1319a8-9000-4bed-b676-3cfd08b473b2.png)
```
import random

def play():
    user = input("what's your choice? 'r' for rock, 'p' for paper, 's' for scissors\n")
    computer = random.choice(['r', 'p', 's'])

    if user == computer:
        return 'It\'s a tie'
    # r > s, s > p, p > r
    if is_win(user, computer):
        return 'You won!'

    return 'you lost!'
def is_win(player, opponent):
    # return true if player wins
    # r > s, s > p, p > r
    if (player == 'r' and opponent == 's') or (player == 's' and opponent == 'p') \
        or (player == 'p' and opponent == 'r'):
        return True

print(play())
```


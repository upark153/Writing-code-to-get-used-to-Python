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



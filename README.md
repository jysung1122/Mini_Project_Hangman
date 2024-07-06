# Mini_Project_Hangman

2024.07.05 ~

### Flow Chart
<img width="588" alt="Solution+-+Hangman+Flowchart+1" src="https://github.com/jysung1122/Python_mini_project/assets/56614779/254cf0ba-bb5d-41b1-8300-1f0e1b8bbfae">

## 개발 순서

### 1. 무작위 단어를 고르고 정답 확인하기
```
#Step 1

import random
word_list = ["aardvark", "baboon", "camel"]

chosen_word = random.choice(word_list)

guess = input("Guess a letter: ").lower()

for i in range(len(chosen_word)) :
    if guess == chosen_word[i] :
        print("Right")
    else :
        print("Wrong")
```

### 2. 빈칸을 맞춘 글자로 변환하기

```
#Step 2

import random
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

guess = input("Guess a letter: ").lower()
display = []
for i in range(len(chosen_word)) :
    display.append("_")

for i in range(len(chosen_word)) :
    if guess == chosen_word[i] :
        display[i] = guess

print(display)
```

### 3. 플레이어가 이겼는지 확인하기
```
#Step 3

import random
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)
word_length = len(chosen_word)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

while True :
    
    guess = input("Guess a letter: ").lower()
    
    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        if letter == guess:
            display[position] = letter

    print(display)

    if "_" not in display :
        print("You win!")
        break
```

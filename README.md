# Mini_Project_Hangman

2024.07.05 ~

### Flow Chart
<img width="588" alt="Solution+-+Hangman+Flowchart+1" src="https://github.com/jysung1122/Python_mini_project/assets/56614779/254cf0ba-bb5d-41b1-8300-1f0e1b8bbfae">

## 개발 순서

### 1. 무작위 단어를 고르고 정답 확인하기
```
#Step 1

word_list = ["aardvark", "baboon", "camel"]

#TODO-1 - Randomly choose a word from the word_list and assign it to a variable called chosen_word.
import random

chosen_word = random.choice(word_list)

#TODO-2 - Ask the user to guess a letter and assign their answer to a variable called guess. Make guess lowercase.
guess = input("Guess a letter: ").lower()

#TODO-3 - Check if the letter the user guessed (guess) is one of the letters in the chosen_word.
for i in range(len(chosen_word)) :
    if guess == chosen_word[i] :
        print("Right")
    else :
        print("Wrong")
```

### 2. 빈칸을 맞춘 글자로 변환하기

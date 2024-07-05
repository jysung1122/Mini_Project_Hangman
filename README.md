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

```
#Step 2

import random
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#TODO-1: - Create an empty List called display.
#For each letter in the chosen_word, add a "_" to 'display'.
#So if the chosen_word was "apple", display should be ["_", "_", "_", "_", "_"] with 5 "_" representing each letter to guess.

guess = input("Guess a letter: ").lower()
display = []
for i in range(len(chosen_word)) :
    display.append("_")

#TODO-2: - Loop through each position in the chosen_word;
#If the letter at that position matches 'guess' then reveal that letter in the display at that position.
#e.g. If the user guessed "p" and the chosen word was "apple", then display should be ["_", "p", "p", "_", "_"].
for i in range(len(chosen_word)) :
    if guess == chosen_word[i] :
        display[i] = guess

#TODO-3: - Print 'display' and you should see the guessed letter in the correct position and every other letter replace with "_".
#Hint - Don't worry about getting the user to guess the next letter. We'll tackle that in step 3.
print(display)
```

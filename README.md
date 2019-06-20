# numbergame-
#Number game app


import random
randomNumber = random.randint(1,10)

print('guess a number between 1 and 10')

trial = 0

while trial < 5:

    try:
        guess = int(input('you guess a number'))
        trial += 1

        if guess == randomNumber:
            print("you got it ")

            if trial == 1:
                print("you are amazing!")
                print("you got it in a single shot!")
            elif trial < 4 and trial > 1:
                print("you are a good guesser!")
                print("you got it in {} tries".format(trial))
            else:
                print("you got it in {} tries".format(trial))

            print('The number that i was thinking is : ', randomNumber)
            exit()
        elif guess not in range(1,10):
            print(" That's not a valid number, please try again! ")

        elif guess > randomNumber:
            print("please try lesser number!")

        elif guess < randomNumber:
            print('please try greater number!')

       
    except ValueError:
        print(" It's not Valid, Please try again, it has to be an integer!")
        continue

print('\n')
print('you missed it!')

print("oh sorry you run out of guesses")
print(' The number that i was thinking is : ', randomNumber)





# print('that is the number')






















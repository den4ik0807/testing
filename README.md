import random
random_number = random.randint(1,100)
attempts = 10
i = 0
print("Это казино и Вы должны угадать задуманное число от 1 до 100! У Вас есть 10 попыток")
while attempts > 0:
    person_number = int(input("Введите число, которое считаете загаданным:"))
    if person_number > random_number:
        all_attempts = i + 1
        attempts = attempts - 1
        print("Вы не угадали число, но было близко, попробуйте меньше:")
        print("Осталось попыток:", attempts)
        i = i + 1
    if person_number < random_number:
        all_attempts = i + 1
        attempts = attempts - 1
        print("Вы не угадали число, но были близко, попробуйте больше:")
        print("Осталось попыток:", attempts)
        i = i + 1
    if attempts == 0:
        print("У Вас не осталось попыток.")
    if person_number == random_number:
        all_attempts = i + 1
        print("Вы угадали задуманное число, поздравляем!")
        print("Вы потратили", all_attempts, "попыток")

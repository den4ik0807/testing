Казино

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

        

Сердце из звездочек

 a = 8
 b = a + 1
 for i in range(a // 2 - 1):
     for j in range(b):
         if i == a // 2 - 2 and (j == 0 or j == b - 1):
             print("*", end=" ")
         elif j <= b // 2 and ((i + j == a // 2 - 3 and j <= b // 4) \
                               or (j - i == b // 2 - a // 2 + 3 and j > b // 4)):
             print("*", end=" ")
         elif j > b // 2 and ((i + j == a // 2 - 3 + b // 2 and j < 3 * b // 4) \
                              or (j - i == b // 2 - a // 2 + 3 + b // 2 and j >= 3 * b // 4)):
             print("*", end=" ")
         else:
             print(" ", end=" ")
     print()
 for i in range(a // 2 - 1, a):
     for j in range(b):
         if (i - j == a // 2 - 1) or (i + j == a - 1 + b // 2):
             print('*', end=" ")
         elif i == a // 2 - 1:
             if j == b // 2 - 3:
                 print('У', end=" ")
             elif j == b // 2-2:
                 print('н', end=" ")
             elif j == b // 2-1:
                 print('и', end=" ")
             elif j == b // 2:
                 print('к', end=" ")
             elif j == b // 2+1:
                 print('У', end=" ")
             elif j == b // 2+2:
                 print('м', end=" ")
             else:
                 print('!', end=" ")
         else:
             print(' ', end=" ")
     print()

     



Пиццерия

print("Добро пожаловать в наше кафе!")
result = 0
i = 0
print("Для начала авторизуйтесь")
parol = input("Придумайте пароль:")
parol_2 = input("Повторите пароль для надежности:")
while parol != parol_2:
    print("Пароли не сходятся, попробуйте еще раз")
    parol_2 = input("Повторите пароль для надежности:")
if parol == parol_2:
    print("Отлично, пароль зарегистрирован")
while i <= 1000:
    choice = input("продолжить выбор пицц?(да/нет)")
    while choice != "нет":
        change = int(input("Гавайская - 1, Дары Моря - 2, Барбекю - 3, Пепперони - 4, Маргарита - 5:    "))
        if change > 5:
            print("Неверный выбор")
        if change == 1:
            size = int(input("Тонкое тесто - 1, Стандартное тесто - 2, Борты с начинкой - 3:    "))
            if size > 3:
                print("Неверный выбор")
            if size == 1:
                price = str(input("Стоимость выбранной пиццы составляет: 699.99 рублей. Добавить в корзину (да/нет)"))
                money = 699.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            elif size == 2:
                price = str(input("Стоимость выбранной пиццы составляет: 399.99 рублей. Добавить в корзину (да/нет)"))
                money = 399.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            else:
                price = str(input("Стоимость выбранной пиццы составляет: 899.99 рублей. Добавить в корзину (да/нет)"))
                money = 899.99
                if price == "да":
                    result = result + money
                else:
                    result = result
        elif change == 2:
            size = int(input("Тонкое тесто - 1, Стандартное тесто - 2, Борт с начинкой - 3:    "))
            if size > 3:
                print("Неверный выбор")
            if size == 1:
                price = str(input("Стоимость выбранной пиццы составляет: 499.99 рублей. Добавить в корзину (да/нет)"))
                money = 499.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            elif size == 2:
                price = str(input("Стоимость выбранной пиццы составляет: 399.99 рублей. Добавить в корзину (да/нет)"))
                money = 399.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            else:
                price = str(input("Стоимость выбранной пиццы составляет: 899.99 рублей. Добавить в корзину (да/нет)"))
                money = 899.99
                if price == "да":
                    result = result + money
                else:
                    result = result
        elif change == 3:
            size = int(input("Тонкое тесто - 1, Стандартное тесто - 2, Борт с начинкой - 3:    "))
            if size > 3:
                print("Неверный выбор")
            if size == 1:
                price = str(input("Стоимость выбранной пиццы составляет: 599.99 рублей. Добавить в корзину (да/нет)"))
                money = 599.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            elif size == 2:
                price = str(input("Стоимость выбранной пиццы составляет: 399.99 рублей. Добавить в корзину (да/нет)"))
                money = 399.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            else:
                price = str(input("Стоимость выбранной пиццы составляет: 899.99 рублей. Добавить в корзину (да/нет)"))
                money = 899.99
                if price == "да":
                    result = result + money
                else:
                    result = result
        elif change == 4:
            size = int(input("Тонкое тесто - 1, Стандартное тесто - 2, Борт с начинкой - 3:    "))
            if size > 3:
                print("Неверный выбор")
            if size == 1:
                price = str(input("Стоимость выбранной пиццы составляет: 599.99 рублей. Добавить в корзину (да/нет)"))
                money = 599.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            elif size == 2:
                price = str(input("Стоимость выбранной пиццы составляет: 399.99 рублей. Добавить в корзину (да/нет)"))
                money = 399.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            else:
                price = str(input("Стоимость выбранной пиццы составляет: 899.99 рублей. Добавить в корзину (да/нет)"))
                money = 899.99
                if price == "да":
                    result = result + money
                else:
                    result = result
        elif change == 5:
            size = int(input("Тонкое тесто - 1, Стандартное тесто - 2, Борт с начинкой - 3:    "))
            if size > 3:
                print("Неверный выбор")
            if size == 1:
                price = str(input("Стоимость выбранной пиццы составляет: 599.99 рублей. Добавить в корзину (да/нет)"))
                money = 599.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            elif size == 2:
                price = str(input("Стоимость выбранной пиццы составляет: 399.99 рублей. Добавить в корзину (да/нет)"))
                money = 399.99
                if price == "да":
                    result = result + money
                else:
                    result = result
            else:
                price = str(input("Стоимость выбранной пиццы составляет: 899.99 рублей. Добавить в корзину (да/нет)"))
                money = 899.99
                if price == "да":
                    result = result + money
                else:
                    result = result
        print("Сейчас в корзине:", result,)
        choice = input("продолжить выбор пицц?(да/нет)")
    if choice == "нет":
            print("Выбор завершен.")
    pay = input("Выберите способ оплаты:(нал/безнал)")
    if pay == "безнал":
        print("Сумма к оплате",result)
        print("Оплата прошла успешно, до свидания!")
        break
    if pay == "нал":
        print("Сумма к оплате", result)
        sum = float(input("Введите вашу сумму:"))
        if sum < result:
            print("У вас не достаточно средств")
        if sum > result:
            lease = sum - result
            print("Ваша сдача:",lease,". До свидания!")
            break
















MVS

# model.py
shoe_inventory = []

def add_shoe(brand, model, size):
    shoe = {"brand": brand, "model": model, "size": size}
    shoe_inventory.append(shoe)

def remove_shoe(index):
    if 0 <= index < len(shoe_inventory):
        removed_shoe = shoe_inventory.pop(index)
        return removed_shoe
    else:
        return None

def get_all_shoes():
    return shoe_inventory


# view.py
def display_menu():
    print("1. Посмотреть все товары")
    print("2. Добавить товар")
    print("3. Удалить товар")
    print("4. Выйти")

def display_all_shoes(shoe_inventory):
    print("\nОбувной инвентарь:")
    for i, shoe in enumerate(shoe_inventory):
        print(f"{i+1}. {shoe['brand']} {shoe['model']}, Размер: {shoe['size']}")

def display_success(message):
    print(f"\nУспешно: {message}")

def display_error(message):
    print(f"\nОшибка: {message}")


# controller.py
from Model import add_shoe, remove_shoe, get_all_shoes
from View import display_menu, display_all_shoes, display_success, display_error

def main():
    while True:
        display_menu()
        choice = input("\nВыберите действие (1-4): ")

        if choice == "1":
            display_all_shoes(get_all_shoes())
        elif choice == "2":
            brand = input("Введите бренд обуви: ")
            model = input("Введите модель обуви: ")
            size = input("Введите размер обуви: ")

            add_shoe(brand, model, size)
            display_success("Обувь успешно добавлена.")
        elif choice == "3":
            index = int(input("Введите номер обуви для удаления: ")) - 1
            removed_shoe = remove_shoe(index)

            if removed_shoe:
                display_success(f"Обувь {removed_shoe['brand']} {removed_shoe['model']} удалена.")
            else:
                display_error("Неверный номер обуви.")
        elif choice == "4":
            print("Выход из программы.")
            break
        else:
            display_error("Неверный выбор. Пожалуйста, выберите от 1 до 4.")

if __name__ == "__main__":
    main()

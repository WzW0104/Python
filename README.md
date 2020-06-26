# Python
Python 学习项目 

Coffee Machine from JetBrains Academy 
# Code below


water = 400
milk = 540
coffee_beans = 120
cups = 9
money = 550


def show_information():
    print("The coffee machine has:")
    print(water, "of water")
    print(milk, "of milk")
    print(coffee_beans, "of coffee beans")
    print(cups, "of disposable cups")
    print(money, "of money")


while True:
    cur = str(input("Write action (buy, fill, take, remaining, exit):"))
    if cur == "buy":
        num = input("What do you want to buy? 1 - espresso, 2 - latte, 3 - cappuccino, back - to main menu:")
        if num == "1":
            water -= 250
            if water < 0:
                print("Sorry, not enough water!")
                water += 250
                continue
            coffee_beans -= 16
            if coffee_beans < 0:
                print("Sorry, not enough coffee beans!")
                coffee_beans += 16
                continue
            money += 4
        elif num == "2":
            water -= 350
            if water < 0:
                print("Sorry, not enough water!")
                water += 350
                continue
            milk -= 75
            if milk < 0:
                print("Sorry, not enough milk!")
                milk += 75
                continue
            coffee_beans -= 20
            if coffee_beans < 0:
                print("Sorry, not enough coffee beans!")
                coffee_beans += 20
                continue
            money += 7
        elif num == "3":
            water -= 200
            if water < 0:
                print("Sorry, not enough water!")
                water += 200
                continue
            milk -= 100
            if milk < 0:
                print("Sorry, not enough milk!")
                milk += 100
                continue
            coffee_beans -= 12
            if coffee_beans < 0:
                print("Sorry, not enough coffee beans!")
                coffee_beans += 12
                continue
            money += 6
        elif num == "back":
            continue
        cups -= 1
        print("I have enough resources, making you a coffee!")
    elif cur == "fill":
        water += int(input("Write how many ml of water do you want to add:"))
        milk += int(input("Write how many ml of milk do you want to add:"))
        coffee_beans += int(input("Write how many grams of coffee beans do you want to add:"))
        cups += int(input("Write how many disposable cups of coffee do you want to add:"))
    elif cur == "take":
        print("I gave you $", money)
        money = 0
    elif cur == "remaining":
        show_information()
    elif cur == "exit":
        break


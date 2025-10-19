import random

class Human:
    def __init__(self, name):
        self.name = name
        self.energy = 50
        self.hunger = 50
        self.money = 100
        self.pet = None

    def eat(self):
        self.hunger += 20
        self.money -= 10
        print(self.name, "поел и стал сытее.")

    def sleep(self):
        self.energy += 30
        self.hunger -= 10
        print(self.name, "поспал и восстановил энергию.")

    def work(self):
        self.money += 25
        self.energy -= 15
        print(self.name, "поработал и заработал денег.")

    def adopt_pet(self, pet):
        self.pet = pet
        print(self.name, "завёл питомца по имени", pet.name)

    def live_day(self):
        if self.hunger < 30:
            self.eat()
        elif self.energy < 30:
            self.sleep()
        else:
            action = random.choice(["work", "eat", "sleep"])
            if action == "work":
                self.work()
            elif action == "eat":
                self.eat()
            else:
                self.sleep()
        if self.pet:
            self.pet.live_day()

class Pet:
    def __init__(self, name):
        self.name = name
        self.hunger = 50
        self.energy = 50

    def eat(self):
        self.hunger += 20
        print(self.name, "поел и доволен.")

    def play(self):
        self.energy -= 10
        self.hunger -= 5
        print(self.name, "играет и веселится.")

    def sleep(self):
        self.energy += 20
        print(self.name, "спит и набирается сил.")

    def live_day(self):
        if self.hunger < 30:
            self.eat()
        elif self.energy < 30:
            self.sleep()
        else:
            action = random.choice(["eat", "sleep", "play"])
            if action == "eat":
                self.eat()
            elif action == "sleep":
                self.sleep()
            else:
                self.play()

person = Human("Рома")
pet = Pet("Бублик")
person.adopt_pet(pet)

for day in range(5):
    print("День", day + 1)
    person.live_day()

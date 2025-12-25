# This class stores a product's name, code and price
class Product:
    def __init__(self, name, code, price):
        self.name = name
        self.code = code
        self.price = price

# This class keeps control on the Vending Machine
class VendingMachine:
    def __init__(self):
        self.name = "Meed Vending Machine"        # Name of the Vending Machine

        # items inside the Vending Machine
        self.products = [
            Product("Maltese chocolate","#10", 4.75),
            Product("Bounty Chocolate","#11", 3.90),
            Product("Bueno chocolate","#12", 4.75),
            Product("Mountain Dew","#13", 4),
            Product("Galaxy Flutes Chocolate", "#14", 4.75),
            Product("Snickers chocolate","#15", 3.90),
            Product("Doritos","#16", 3.50),
            Product("Oreo","#17", 2.95),
            Product("Galaxy Bar","#18", 5.50),
            Product("Water","#19", 1.50),
            Product("KitKat","#20", 3.50),
            Product("Halley Biscuit","#21", 3.50),
            Product("Apple Juice ","#22", 3.50),
            Product("Ice Tea","#23", 5.50),
            Product("Chocolate Milk","#24", 2.50),
            Product("Sabahoo cake","#25", 3.50)
        ]

    # this is the UI(user interface) for the user
    def show_products(self):
        print("Welcome to Meed Vending Machine!")
        print("Code  Name                    Price")
        print("----------------------------------------")

        # this code shows all the items in the Vending Machine one by one
        for p in self.products:
            code = p.code + " " * (6 - len(p.code))
            name = p.name + " " * (25 - len(p.name))
            price = str(p.price)
            print(code + name + price)

    # This code helps the user to buy something
    def buy(self):
        code = input("Enter product code: ")         # This code ask the user to enter product code in the Vending Machine

        for p in self.products:
            if p.code == code:
                print("You selected: " + p.name)
                print("Price: " + str(p.price) + " SAR")

                money = float(input("Insert money: "))      # This code ask the user to insert the money

                # This code checks that the price is low or high 
                if money < p.price:
                    print("Not enough money. Product not dispensed.")
                    return

                # This code gives the rest of the money after buying a specific product
                change = money - p.price
                print("Dispensing " + p.name + "...")
                print("Change returned: " + str(change) + " SAR")
                print("Thank you for using meed Vending Maching!")
                return

        # if the product code is wrong
        print("Invalid code.")

# Starting the Vending Maching
machine = VendingMachine()
machine.show_products()
machine.buy()

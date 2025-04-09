# OOP-Assignment.py


#QUETION 1

#  Base class representing a general Smartphone
class Smartphone:
    # Constructor to initialize smartphone attributes
    def __init__(self, brand, model, storage, battery):
        self.brand = brand            # Brand of the smartphone
        self.model = model            # Model name/number
        self.storage = storage        # Storage in GB
        self.battery = battery        # Battery capacity

    # Method to return basic smartphone info
    def get_info(self):
        return f"{self.brand} {self.model} with {self.storage}GB storage and {self.battery}mAh battery."
#2
# Subclass representing a Gaming Smartphone
class GamingSmartphone(Smartphone):
    # Using __init__ constructor
    def __init__(self, brand, model, storage, battery):
        super().__init__(brand, model, storage, battery)  # Calling the parent constructor
        

    # Polymorphism
    def get_info(self):
        return f"{self.brand} {self.model} (Gaming Edition) with {self.storage}GB storage, {self.battery}mAh battery."

#3
# Creating a regular smartphone instance
phone1 = Smartphone("Samsung", "Galaxy A52", 64, 4500)

# Creating a gaming smartphone instance for the child class
gaming_phone = GamingSmartphone("ASUS", "ROG Phone 5", 256, 6000)

# Displaying information
print(phone1.get_info())         # Calls method from Smartphone class
print(gaming_phone.get_info())   # Calls overridden method from GamingSmartphone

# Checking storage
print(phone1.storage)      
print(gaming_phone.storage) 

# Checking battery
print(phone1.battery)
print(gaming_phone.battery)

# Checking brand
print(phone1.brand)
print(gaming_phone.brand)

# Checking model
print(phone1.model)
print(gaming_phone.model)

# Checking class type
print(type(phone1))              # Output: <class '__main__.Smartphone'>
print(type(gaming_phone))        # Output: <class '__main__.GamingSmartphone'>




# QUESTION 2

#  Base class for all vehicles
class Vehicle:
    def move(self):
        # This method will be overridden by each child class
        pass


# Car class
class Car(Vehicle):
    def move(self):
        print("The card is being Driven")

# Plane class
class Plane(Vehicle):
    def move(self):
        print("The plane is flying ")

# Boat class
class Boat(Vehicle):
    def move(self):
        print("The boat is Sailing ")

# Bicycle class
class Bicycle(Vehicle):
    def move(self):
        print("Tonny Onwonga is Pedaling ")

# Create a list of different vehicles
vehicles = [Car(), Plane(), Boat(), Bicycle()]

# Loop through and call move() on each vehicle
for x in vehicles:
    x.move()


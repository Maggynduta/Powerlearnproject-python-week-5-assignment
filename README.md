# Powerlearnproject-python-week-5-assignment
activity 1:
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def get_details(self):
        return f"{self.brand} {self.model} costs ${self.price}"

    def make_call(self, number):
        return f"Calling {number} from {self.model}..."

class Smartwatch(Smartphone):  # Inheriting from Smartphone
    def __init__(self, brand, model, price, health_tracking):
        super().__init__(brand, model, price)
        self.health_tracking = health_tracking

    def get_details(self):
        return f"{self.brand} {self.model} (Smartwatch) - Health tracking: {self.health_tracking}"

# Example usage
phone = Smartphone("Samsung", "Galaxy S22", 999)
watch = Smartwatch("Apple", "Watch Series 7", 399, True)

print(phone.get_details())
print(phone.make_call("+123456789"))
print(watch.get_details())

activity 2:
class Vehicle:
    def move(self):
        pass  # This will be overridden by subclasses

class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

class Boat(Vehicle):
    def move(self):
        return "Sailing 🚢"

# Example usage
vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    print(v.move())  # Each calls its own move() method

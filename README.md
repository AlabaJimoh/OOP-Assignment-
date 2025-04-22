# OOP-Assignment-
class Smartphone:
    def __init__(self, brand, model, screen_size, storage, color, battery_life):
        self.brand = brand
        self.model = model
        self.screen_size = screen_size  # in inches
        self.storage = storage            # in GB
        self.color = color
        self.battery_life = battery_life  # in hours

    def make_call(self, number):
        return f"Calling {number} from {self.brand} {self.model}."

    def send_message(self, recipient, message):
        return f"Sending message to {recipient}: {message}"

    def take_photo(self):
        return f"Taking a photo with {self.brand} {self.model}."

    def play_music(self, song):
        return f"Playing {song} on {self.brand} {self.model}."

class SamsungS24(Smartphone):
    def __init__(self, model, color):
        super().__init__("Samsung", model, 6.1, 128, color, 12)

    def take_photo(self):
        return f"Taking a high-resolution photo with the Samsung Galaxy S24's camera."

class IPhone15(Smartphone):
    def __init__(self, model, color):
        super().__init__("Apple", model, 6.1, 128, color, 10)

    def take_photo(self):
        return f"Taking a stunning photo with the iPhone 15's advanced camera."

# Create instances
samsung = SamsungS24("Galaxy S24", "Phantom Black")
iphone = IPhone15("iPhone 15", "Midnight")

# Demonstrate methods
print(samsung.make_call("123-456-7890"))
print(samsung.send_message("Alaba", "Hello!"))
print(samsung.take_photo())
print(samsung.play_music("Song A"))

print(iphone.make_call("0987-654-321"))
print(iphone.send_message("Jimoh", "Hi there!"))
print(iphone.take_photo())

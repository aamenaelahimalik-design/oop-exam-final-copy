##Restaurant Menu Manager – GitHub Repository Package

## Repository Structure
restaurant-menu-manager/
│
├── README.md
└── menu_manager.py
## README.md
## Restaurant Menu Manager
A simple Python program that lets you:
- Add menu items
- Update existing menu items
- Display the entire menu


This project uses OOP concepts such as classes and methods.


## How to Run
1. Make sure you have Python installed.
2. Run the script using:


```bash
python menu_manager.py
Features

Menu items stored as objects

No float prices (only integers allowed)

Easy to update and display menu

Example Output
Added: Biryani: Rs. 250 (Main Course)
Added: Raita: Rs. 30 (Side)
Added: Chai: Rs. 50 (Drink)


--- Restaurant Menu ---
Biryani: Rs. 250 (Main Course)
Raita: Rs. 30 (Side)
Chai: Rs. 50 (Drink)

## menu_manager.py
MenuItem class (only int price allowed)

class MenuItem: def init(self, name, price, category): self.name = name self.price = price # price must be integer self.category = category

# Update item details
def update(self, price, category):
    self.price = price
    self.category = category


def __str__(self):
    return f"{self.name}: Rs. {self.price} ({self.category})"
MenuManager class to handle the menu

class MenuManager: def init(self): self.menu = {} # dictionary to store items

# Add a new item to the menu
def add_item(self, name, price, category):
    self.menu[name] = MenuItem(name, price, category)
    print(f"Added: {self.menu[name]}")


# Update an existing menu item
def update_item(self, name, price, category):
    if name in self.menu:
        self.menu[name].update(price, category)
        print(f"Updated: {self.menu[name]}")
    else:
        print(f"Item '{name}' not found in the menu.")


# Display menu details
def display_menu(self):
    print("\n--- Restaurant Menu ---")
    if not self.menu:
        print("Menu is empty.")
    else:
        for item in self.menu.values():
            print(item)
    print("------------------------\n")
Example usage

if name == "main": menu_manager = MenuManager()

menu_manager.add_item("Biryani", 250, "Main Course")
menu_manager.add_item("Raita", 30, "Side")
menu_manager.add_item("Chai", 50, "Drink")


menu_manager.display_menu()


menu_manager.update_item("Chai", 60, "Hot Drink")
menu_manager.display_menu()
✅ Help you step-by-step upload it to GitHub (website method or GitHub Desktop)

Just tell me what you want next!

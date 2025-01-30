# Restaurant Menu System

A simple Python project to simulate a restaurant menu system, supporting multiple menus, franchises, and billing calculations.

## Overview

This system allows you to manage different types of menus for various times of day and calculate the total bill based on the items selected by customers. It was developed to represent a fictional restaurant, but it can be easily adapted for any establishment looking to organize its dishes and services. 

The system is designed using object-oriented programming principles, with classes representing the menus, franchises, and the business itself. This design makes it flexible and extensible, allowing for future expansions such as adding new menu types or franchise locations.

   ## About

This project was developed as part of a Python programming exercise. It showcases the application of object-oriented programming principles, such as creating classes for menu management, franchise handling, and billing calculations. The goal was to build a flexible system that could be expanded easily and used in various restaurant scenarios.

## Features

- **Flexible Menu Management**  
  The system supports different menus for various times of day (e.g., brunch, dinner, kids' menu, desserts). Each menu has a set of items (dishes and drinks) with predefined prices, making it easy to manage multiple menu options based on the time.

- **Bill Calculation**  
  The system can calculate the total price of an order based on a list of items purchased from the menu. By passing the list of items to the `calculate_bill()` method, you can easily determine the total bill for a customer.

- **Franchise and Location Management**  
  You can create multiple franchises, each with its own set of menus. This allows the system to simulate a business with different locations, making it suitable for restaurant chains.

- **Menu Availability Check**  
  The system can check which menus are available at a specific time. Using the `available_menus(time)` method, you can determine whether the brunch, dinner, or dessert menu is available at a given hour. The system takes into account the predefined time frames for each menu, such as brunch being available from 9 AM to 12 PM, and dessert being available from 8 PM to 11 PM.

- **Extensible Structure**  
  The code is designed in a modular way, making it easy to add more menus, items, or franchises. If a new menu or location is required, you can easily extend the system by adding new instances of the `Menu` or `Franchise` classes.

## How to Use

1. **Define Your Menus**  
   Create your menus by specifying their name, items, and available time ranges. For example:
   ```python
   brunch_items = {
       'apple pie': 8.00,
       'croissant': 5.50,
       'mushroom omelet': 10.00
   }
   brunch = Menu('Morning Sweetness', brunch_items, '9am', '12pm')
   ```

2. **Assign Menus to Franchises**  
   Create franchises and assign the relevant menus to them. Each franchise can have different menus available based on the time of day.
   ```python
   flagship_store = Franchise('123 Happiness Avenue', [brunch, dinner, kids_menu])
   ```

3. **Calculate the Total Bill**  
   Use the `calculate_bill()` method to calculate the total for a list of items purchased by a customer.
   ```python
   dessert_order = ['tiramisu', 'cannoli']
   total_bill = dessert_menu.calculate_bill(dessert_order)
   print(f'Total bill for dessert: ${total_bill}')
   ```

4. **Check Available Menus**  
   Use the `available_menus(time)` method to check which menus are available at a given time of day.
   ```python
   available_menus = flagship_store.available_menus('9pm')
   print(available_menus)
   ```

## Example Usage

```python
# Define menus for different times of day
dessert_items = {'tiramisu': 6.50, 'cannoli': 5.00}
dessert_menu = Menu('Dessert Delights', dessert_items, '8pm', '11pm')

brunch_items = {'apple pie': 8.00, 'croissant': 5.50}
brunch = Menu('Morning Sweetness', brunch_items, '9am', '12pm')

# Create franchise and assign menus
flagship_store = Franchise('123 Happiness Avenue', [brunch, dessert_menu])

# Check available menus at a specific time
print(flagship_store.available_menus('9pm'))  # Should show brunch and dessert menus
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Restaurant-Menu-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Restaurant-Menu-System
   ```
3. Run the script:
   ```bash
   python menu_system.py
   ```

## License

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.

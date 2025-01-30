# Restaurant Menu System

A simple Python project to simulate a restaurant menu system, supporting multiple menus, franchises, and billing calculations.

## Countdown

- **4. Franchises Management**  
  Create multiple franchises and assign menus to them. Easily manage different locations with unique menu items.
  
- **3. Menu Availability by Time**  
  Check which menus are available based on the time of day. The system knows when to serve brunch, dinner, and desserts!

- **2. Bill Calculation**  
  Calculate the total price of a customer’s order by simply listing the items purchased from the menu. 

- **1. Flexible Menu Structure**  
  Supports multiple menus, including brunch, dinner, kids, and desserts, each with customizable items and prices.

## How to Use:

1. Define your menus with names, items, and prices.
2. Assign menus to franchises, specifying their available times.
3. Use the `calculate_bill()` method to calculate the total for a list of items purchased by a customer.
4. Use the `available_menus(time)` method to check which menus are available at a given time of day.

## Installation:

Clone the repository and run the `menu_system.py` script to test the functionality.

```bash
git clone https://github.com/yourusername/Restaurant-Menu-System.git
cd Restaurant-Menu-System
python menu_system.py

## License:
This project is licensed under the Apache 2.0 License - see the LICENSE file for details.
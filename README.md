# Restaurant Billing System (Python)

This is a simple console-based restaurant billing system built using Python.  
The program displays a menu, allows users to select food items with quantities, 
and calculates the total bill.

## Features
- Menu stored using Python dictionary
- Item selection with quantity
- Automatic bill calculation
- User-friendly console interaction

## Technologies Used
- Python

## Suitable For
- Python beginners
- Practice with dictionaries, loops, and input/output


menu = {
    1: ("burger:", 50),
    2: ("pizza:", 200),
    3: ("cold coffee:", 120),
    4: ("pasta", 150)
}

total_bill = 0
print("menu")

for i, (item_name, price) in menu.items():
    print(i, ".", item_name, "- ₹", price)

print("select item and quantity ")
print("0 for bill")

while True:
    x = int(input("enter item number: "))
    # item_no = int(input("enter item number: "))
    if x == 0:
        break
    elif x in menu:
        qty = int(input("Enter quantity: "))
        item_name, price = menu[x]
        subtotal = price * qty
        print(item_name, "added | Subtotal: ₹", subtotal)
        total_bill += subtotal   


    elif x in menu:
        total_bill += menu[x][1]
        print(menu[x][0])
    else:
        print("invalid  ")

print("total bill = ₹", total_bill)


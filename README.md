# Cafe Billing System

This is a graphical user interface (GUI) application for a coffee shop billing system. Built using Python's `tkinter` library, it allows the user to select items (coffee and non-coffee beverages), calculate the total cost, generate a detailed bill, and share it via WhatsApp or save it locally. It also includes tax calculations and a clean user interface for input and billing display.

## Features
1. **Itemized Bill Calculation**: 
    - The system allows customers to select the quantity of various coffee and non-coffee items. It calculates the subtotal, taxes (SGST and CGST), and the grand total.
  
2. **Billing Area**:
    - A billing area is dynamically populated with items, prices, and quantities, and the total cost is displayed at the bottom.
  
3. **Customer Information**:
    - The customer’s name and phone number are required before generating the bill.

4. **WhatsApp Sharing**:
    - Once the bill is generated, it can be shared via WhatsApp by opening the default web browser with the encoded bill content ready to be sent to the customer's WhatsApp number.

5. **Saving and Printing Bills**:
    - The bill can be saved locally as a text file in a "bills" folder, and it can also be printed using system print utilities.

6. **Clear All Fields**:
    - Users can reset all inputs, clearing both the item entries and the billing area.

---

## How It Works

### 1. **Item Selection and Price Calculation**
Each item (coffee and non-coffee beverages) has an entry box for the user to input the quantity. The total cost is calculated based on the fixed price of each item. The `total()` function handles the following:
   - Calculates the total price for coffee items.
   - Calculates the total price for non-coffee items.
   - Computes the subtotal by summing the prices of all selected items.
   - Computes the tax (18% in total, divided equally between SGST and CGST).
   - Computes the grand total (subtotal + tax).

### 2. **Bill Generation**
Once the items and customer information have been input, the `bill_area()` function generates a detailed bill in the text area. It includes:
   - Current date and time.
   - Bill number (randomly generated).
   - Customer name and phone number.
   - A detailed itemized list of selected products along with their quantity and price.
   - Subtotal, tax breakdown (SGST & CGST), and the grand total.
   - A friendly thank you message at the bottom.

### 3. **Saving the Bill**
The `save_bill()` function allows the user to save the bill as a `.txt` file. The file name is the bill number, and the bill is saved in a "bills" folder.

### 4. **Sharing the Bill via WhatsApp**
The `share_on_whatsapp()` function encodes the bill content and opens the WhatsApp web link in the default browser, pre-filled with the customer’s phone number and the bill details. This allows easy sharing with customers.

### 5. **Printing the Bill**
The `print_bill()` function creates a temporary text file containing the bill and opens the system's default print utility to print the bill.

### 6. **Clear All Fields**
The `clear_all()` function resets all the entry fields and the billing area, allowing the user to start fresh for a new customer.

---

## GUI Components Breakdown

- **Main Window**: 
  - The window is titled "Billing System" and is maximized using the `zoomed` state.
  
- **Header**:
  - A label displaying "#COFFEE SHOP" with custom styling is placed at the top of the window.
  
- **Customer Information Section**:
  - A labeled frame where the customer inputs their name and phone number.
  
- **Items Section**:
  - The GUI contains two sections: one for coffee and one for non-coffee items. Each section includes item labels and corresponding entry fields for quantity.
  
- **Billing Area**:
  - A text area within a frame where the generated bill is displayed. It also includes a scroll bar for easy navigation of the bill content.
  
- **Summary and Total Section**:
  - The bottom part of the GUI displays the cost of coffee, non-coffee items, subtotal, tax, and the grand total.

- **Button Section**:
  - The GUI has buttons to calculate totals, generate the bill, save the bill, print the bill, share it on WhatsApp, and clear all fields.

---

## Requirements

- Python 3.x
- `tkinter` (comes pre-installed with Python)
- `random`, `tempfile`, `webbrowser`, `urllib.parse`, and `datetime` (all standard Python libraries)

---

## Future Improvements
- **Item customization**: Add more flexibility in item selection with a customizable menu.
- **Database support**: Store and retrieve customer bills using a database.
- **Print functionality on non-Windows systems**: Ensure the print function works seamlessly across all operating systems.

---

Feel free to contribute by submitting issues or pull requests!

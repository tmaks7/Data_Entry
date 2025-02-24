# Data_Entry and Validation Project
This is an end to end data entry project using Excel

## Overview
This project demonstrates data entry automation, validation, and dynamic data retrieval in Excel. It consists of two primary sheets: Sales and Inventory, which are interconnected to streamline stock management and sales tracking. The project utilizes Excel functions such as Data Validation, Conditional Formatting Lookup Functions (VLOOKUP), and Logical Functions (SUMIF) to enhance accuracy and efficiency.

## Features
* Automated Price Retrieval: Whenever a product is entered in the Sales sheet, its price is automatically fetched from the Inventory sheet.

* Stock Monitoring: The Inventory sheet dynamically updates based on sales transactions, showing out-of-stock products.

* Data Validation: Ensures correct entry of dates, payment details, and numerical values.

* Logical Conditions: Calculates outstanding balance, excess payments, and debt tracking.

  ## Data Structure
  #### Sales Sheet Columns
| Column Name           | Description                                                                  |
|-----------------------|------------------------------------------------------------------------------|
| Date of Transaction   | Records the date of each sale                                              |
| Product/Service Sold  | The name of the sold product/service                                        |
| Quantity              | The quantity of the item sold                                               |
| Price per Unit        | The unit price, auto-fetched from the Inventory sheet                            |
| Total Cost            | Computed as Quantity * Price per Unit                                       |
| Customer Name         | Name of the customer making the purchase                                     |
| Payment Method        | Payment mode (Cash, Transfer, etc.)                                         |
| Paid                  | Checkbox to indicate if payment was made                                    |
| Paid, how much?       | Amount paid by the customer                                                |
| Excess/Debt           | Calculates any excess payment or outstanding debt                               |
| Balance Paid          | Tracks additional payments toward outstanding balances                               |

#### Inventory Sheet Columns
| Column Name           | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| Product/Service Sold  | Name of the product or service                                            |
| Quantity (Pack)       | Available quantity in packs                                               |
| Quantity (Pieces)     | Available quantity in pieces                                              |
| Total Quantity        | Computed as Quantity (Pack) *   Quantity (Pieces)           |
| Price per Unit        | Unit price of the product                                                 |
| Total Cost            | Price of the product from market                                |
| Stock_update          | Adjusts inventory based on sales transactions                               |
| Total Price           | Total stock value in the inventory                                         |

## Functionality
#### 1.  Automatic Price Update:
* When a product is entered in the Sales sheet, the price per unit is automatically fetched from the Inventory sheet using VLOOKUP

#### 2. Real-Time Stock Updates:
* When a product is sold, the inventory count is updated using SUMIF and CONDITIONAL FORMATTING functions

#### 3. Payment Tracking & Debt Management:
* If the amount paid is less than the total cost, the system records it as debt
* If the amount paid is more than the total cost, it calculates the excess amount
* The Balance Paid column allows tracking of multiple payments for the same transaction

## How to Use
1. Enter a product in the Sales sheet.

2. The price automatically appears based on inventory records.

3. Enter the quantity sold; total cost is auto-calculated.

4. Input customer payment details, and the system calculates any balance or excess payment.

5. The Inventory sheet updates stock levels in real-time.

6. Out-of-stock products are highlighted for restocking.

## Excel Functions Used
* VLOOKUP: Fetch product prices automatically
* SUMIF: Calculate stock levels and sales totals
* Data Validation: Restricts incorrect data entry
* Conditional Formatting: Implements an automated alert system for low stock levels less than 10

## Future Improvements
* Introduce a user-friendly dashboard for quick sales and inventory insights
* Expand payment tracking to include installment plans

## Conclusion
This project showcases an efficient and automated approach to managing sales and inventory using Excel functions. It enhances accuracy, reduces manual errors, and improves decision-making for small businesses

# controlflow-and-function-in-python
Create a function named calculate_discount(price, discount_percent) that calculates the final price after applying a discount. The function should take the original price (price) and the discount percentage (discount_percent) as parameters. If the discount is 20% or higher, apply the discount; otherwise, return the original price.
Using the calculate_discount function, prompt the user to enter the original price of an item and the discount percentage. Print the final price after applying the discount, or if no discount was applied, print the original price.

def calculate_discount(price, discount_percent):
  """Calculates the final price after applying a discount.

  Args:
    price: The original price of the item.
    discount_percent: The discount percentage (e.g., 10 for 10%).

  Returns:
    The final price after applying the discount, or the original price if
    the discount is less than 20%.
  """
  if discount_percent >= 20:
    discount_amount = (discount_percent / 100) * price
    final_price = price - discount_amount
    return final_price
  else:
    return price

# Get user input
try:
  original_price = float(input("Enter the original price of the item: "))
  discount = float(input("Enter the discount percentage (e.g., 10 for 10%): "))

  # Calculate and print the final price
  final_amount = calculate_discount(original_price, discount)

  if final_amount == original_price:
    print(f"No discount applied. The final price is: {final_amount:.2f} KES")
  else:
    print(f"The final price after applying the discount is: {final_amount:.2f} KES")

except ValueError:
  print("Invalid input. Please enter numeric values for price and discount.")

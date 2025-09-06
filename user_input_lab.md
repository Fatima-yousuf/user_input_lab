# User Input Practice Lab
```python
kg = float(input("Enter weight in kilograms: "))
pounds = kg * 2.2
print("Weight in pounds:", pounds)
```
## Part B: Credit card interest
```python
balance = float(input("Enter balance: "))
payment = float(input("Enter payment: "))
days_in_cycle = int(input("Enter number of days in billing cycle: "))
days_payment_before = int(input("Enter number of days payment was made before billing cycle: "))
interest_rate = float(input("Enter monthly interest rate (e.g., 0.0152): "))

avg_daily_balance = (balance * days_in_cycle - payment * days_payment_before) / days_in_cycle
interest = avg_daily_balance * interest_rate

print("Interest on unpaid balance:", interest)
```
## Part C: Distance between two cars
```python
from math import sqrt

speed_a = float(input("Enter speed of car A (mph): "))
speed_b = float(input("Enter speed of car B (mph): "))
hours = float(input("Enter elapsed hours: "))
minutes = float(input("Enter elapsed minutes: "))

total_hours = hours + minutes / 60
distance_a = speed_a * total_hours
distance_b = speed_b * total_hours

distance_between = sqrt(distance_a**2 + distance_b**2)
print("Distance between cars:", distance_between)
```
## Troubleshooting Variables
- a. hello = "hello" ✅ Valid  
- b. _var = 100 ✅ Valid  
- c. !var_1 = 200 ❌ Invalid: Variable names cannot start with '!'  
- d. print = "print me" ❌ Bad practice: overwrites built-in print()  
- e. False = 0 ❌ Invalid: Cannot assign to Python keywords
## Challenges
Please describe the challenges you faced during the exercise:
One challenge that I encountered with this task dealt with learning how to accurately get the user input and also convert that input into the appropriate data type to perform the calculations as well. Another challenge was making sure that I applied the formulas correctly, particularly for calculating the credit card interest and the distance of the car dynamically, with no errors.

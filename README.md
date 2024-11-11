# Code-Repository-Project
the code repository for the project of the script programming class Fall 2024 Michael Schnell

# Week one code-----------------------------------------------------------------------------------

# Project one
name = input("Enter your name: ")
address = input("Enter your address: ")
phone_number = input("Enter your phone number: ")
print("Name:", name)
print("Address:", address)
print("phone number:", phone_number)

# Project two
width = float(input("Enter the width: "))
length = float(input("Enter the Length: "))
area = width * length
print("The area is", area, "square units.")

# Project three 
base = float(input("Enter the base of the triangle: "))
height = float(input("Enter the height of the triangle: "))
area = .5 * base *height
print("The area of the triangle is", area, "square units.")

# Project four
radius = float(input("Enter the radius of the circle: "))
area = 3.14 * radius ** 2
print("The area of the circle is", area, "square units.")

# Project five
height = float(input("Enter the height of the cuboid: "))
width = float(input("Enter the width of the cuboid: "))
depth = float(input("Enter the depth of the cuboid: "))
volume = height * width * depth
print("The volume of the cuboid is: ", volume, "cubic units.")

# Week two code-----------------------------------------------------------------------------------

# Sphere project
radius = float(input("Enter the radius of the sphere: "))
PI = 3.14
diameter = 2 * radius
circumference = 2 * PI * radius
surfacearea = 4 * PI * radius**2
volume = (4/3) * PI * radius**3
print("Diameter: ", diameter)
print("Circumference: ",circumference)
print("Surfacearea: ", surfacearea)
print("Volume: ", volume)

# Momentum project
mass = float(input("Enter the mass of the object(Kilograms): "))
velocity = float(input("Enter the velocity of the object(meters per second): "))
momentum = mass * velocity
print("The momentum of the object is:", momentum)

# Cube project
edgelength = int(input("Enter the length of the edge of the cube: "))
surfacearea = 6 * (edgelength ** 2)
print("The surface area of the cube is:", surfacearea)

# Week three code-----------------------------------------------------------------------------------

# Project10
hourlywage = float(input("What is the hourly wage?: "))
normalhours = float(input("What is the amount of non-overtime hours for this week?: "))
overtimehours = float(input("What is the amount of overtime hours worked this week?: "))           
regularpay = normalhours * hourlywage
overtimepay = overtimehours * hourlywage * 1.5
totalpay = overtimepay + regularpay
print ("Your total pay for this week is: ",totalpay)

# Project07
years = float(input("Enter the number of years: "))
minutes = years * 365 * 24 * 60
print("There are", minutes, "minutes in", years, "years")

# Week four code-----------------------------------------------------------------------------------

# Population project
startingpopulation = int(input("Enter the starting number of organisms: "))
growthrate = float(input("Enter the growth rate (> 0): "))
hoursforgrowthrate = float(input("Enter the number of hours needed to reach the growth rate stated: "))
totalgrowthtime = float(input("Enter the total number of hours the population will be growing: "))
growthcycles = totalgrowthtime // hoursforgrowthrate
finalpop = startingpopulation * (growthrate ** growthcycles)
print("The population after", totalgrowthtime, "hours is:", finalpop)

# Equilateral project
a = float(input("Enter the length of the first side: "))
b = float(input("Enter the length of the second side: "))
c = float(input("Enter the length of the third side: "))
if a == b ==b:
    print("The triangle is an equilateral.")
else:
    print("The triangle is not an equilateral.")

# Bouncy project
initial_height = float(input("Enter the initial height the ball was dropped from: "))
bounce_index = float(input("Enter the bounciness index (0-1): "))
bounces = int(input("Enter the number of bounces: "))
total_distance = initial_height
height = initial_height
for _ in range(bounces):
    height *= bounce_index
    total_distance += height *2
print("The total distance traveled by the ball is", total_distance)

# Week five code-----------------------------------------------------------------------------------

# Guess
import random
smaller = int(input("Enter the smaller number: "))
larger = int(input("Enter the larger number: "))
print(f"Think of a number between {smaller} and {larger} (inclusive).")
input("Press Enter when you're ready...")
count = 0
low = smaller
high = larger
while True:
    count += 1
    myGuess = random.randint(low, high)
    print("Computer guesses:", myGuess)
    feedback = input("Is the guess too (s)mall, too (l)arge, or (c)orrect? ").lower()
    if feedback == 's':
        print("Guess is too small!")
        low = myGuess + 1
    elif feedback == 'l':
        print("Guess is too large!")
        high = myGuess - 1
    elif feedback == 'c':
        print("Congratulations! The computer got it in", count, "tries!")
        break
    else:
        print("Invalid input. Please enter 's', 'l', or 'c'.")

# Salary project
starting_salary = float(input("Enter the starting salary: "))
percentage_increase = float(input("Enter the percentage increase (as a decimal): "))
years = int(input("Enter the number of years: "))
print("Year | Salary")
print("-----|---------")
for year in range(1, years + 1):
    salary = starting_salary * (1 + percentage_increase) ** (year - 1)
    print(f"{year:4} | ${salary:,.2f}")

# Tidbit project
purchase_price = float(input("Enter the purchase price: "))
down_payment_rate = 0.10
annual_interest_rate = 0.12
monthly_payment_rate = 0.05
down_payment = purchase_price * down_payment_rate
loan_amount = purchase_price - down_payment
monthly_payment = loan_amount * monthly_payment_rate
print("{:<10}{:<20}{:<20}{:<20}{:<20}{:<20}".format(
    "Month", "Total Balance", "Interest Owed", "Principal Owed", "Payment", "Remaining Balance"))
month = 1
total_balance = loan_amount
while total_balance > 0:
    interest_owed = total_balance * (annual_interest_rate / 12)
    principal_owed = monthly_payment - interest_owed
    if principal_owed > total_balance:
        principal_owed = total_balance
        monthly_payment = interest_owed + principal_owed
    remaining_balance = total_balance - principal_owed
    print("{:<10}{:<20.2f}{:<20.2f}{:<20.2f}{:<20.2f}{:<20.2f}".format(
        month, total_balance, interest_owed, principal_owed, monthly_payment, remaining_balance))
    total_balance = remaining_balance
    month += 1

# Week six code---------------------------------------------------------------------------------

# Encrypt project
plaintext = input("Enter the plaintext: ")
distance = int(input("Enter the distance value: "))
encrypted_text = ""
for char in plaintext:
    if ' ' <= char <= '~':
        new_char = chr(((ord(char) - 32 + distance) % 95) + 32)
        encrypted_text += new_char
    else:
        encrypted_text += char
print("Encrypted text:", encrypted_text)

# Decrypt project
ciphertext = input("Enter the ciphertext: ")
distance = int(input("Enter the distance value: "))
decrypted_text = ""
for char in ciphertext:
    if ' ' <= char <= '~':
        new_char = chr(((ord(char) - 32 - distance) % 95) + 32)
        decrypted_text += new_char
    else:
        decrypted_text += char
print("Decrypted text:", decrypted_text)

# Copyfile project
source_file = input("Enter the name of the source file: ")
destination_file = input("Enter the name of the destination file: ")
try:
    with open(source_file, 'r') as src:
        contents = src.read()
    with open(destination_file, 'w') as dest:
        dest.write(contents)
    print(f"Contents copied from '{source_file}' to '{destination_file}' successfully.")
except FileNotFoundError:
    print(f"Error: The file '{source_file}' was not found.")
except Exception as e:
    print(f"An error occurred: {e}")

# Week seven code---------------------------------------------------------------------------------

# Stats project
def mean(numbers):
    if not numbers:
        return 0
    return sum(numbers) / len(numbers)

def median(numbers):
    if not numbers:
        return 0
    sorted_numbers = sorted(numbers)
    n = len(sorted_numbers)
    if n % 2 == 1:
        return sorted_numbers[n // 2]
    else:
        mid1 = sorted_numbers[n // 2 - 1]
        mid2 = sorted_numbers[n // 2]
        return (mid1 + mid2) / 2

def mode(numbers):
    if not numbers:
        return 0
    frequency = {}
    for num in numbers:
        frequency[num] = frequency.get(num, 0) + 1
    max_freq = max(frequency.values())
    modes = [num for num, freq in frequency.items() if freq == max_freq]
    return modes[0] if len(modes) == 1 else modes

def main():
    user_input = input("Enter a list of numbers separated by spaces: ")
    numbers = list(map(int, user_input.split()))
    print(f"Mean: {mean(numbers)}")
    print(f"Median: {median(numbers)}")
    print(f"Mode: {mode(numbers)}")

# Navigate project
filename = input("Enter the filename: ")
with open(filename, 'r') as file:
    lines = file.readlines()

while True:
    print(f"Number of lines in the file: {len(lines)}")
    line_number = int(input("Enter line number (0 to quit): "))
    if line_number == 0:
        break
    if 1 <= line_number <= len(lines):
        print(lines[line_number - 1].strip())
    else:
        print("Invalid line number. Please try again.")

# Week eight code---------------------------------------------------------------------------------

# Average project
For some reason I only have two copies of the testinputfunction project and one copy of the testsort project. This one got lost.


# Testinputfunction project
def read_numbers(filename):
    """Reads numbers from a text file and returns them as a list of floats."""
    with open(filename, 'r') as file:
        numbers = []
        for line in file:
            try:
                numbers.append(float(line.strip()))
            except ValueError:
                print(f"Warning: '{line.strip()}' is not a valid number and will be skipped.")
        return numbers
def compute_average(numbers):
    """Computes the average of a list of numbers."""
    return sum(numbers) / len(numbers) if numbers else 0
def main():
    filename = input("Enter the name of the text file: ")
    try:
        numbers = read_numbers(filename)
        average = compute_average(numbers)
        print(f"The average is: {average}")
    except FileNotFoundError:
        print("Error: File not found.")
if __name__ == "__main__":
    main()


# Testsort project
def isSorted(lst):
    if len(lst) < 2:
        return True
    for i in range(len(lst) - 1):
        if lst[i] > lst[i + 1]:
            return False
    return True
user_input = input("Enter a list of numbers separated by spaces: ")
number_list = list(map(int, user_input.split()))
result = isSorted(number_list)
print(f"The list {number_list} -> isSorted: {result}")

# Week nine code---------------------------------------------------------------------------------

# Circle project
import turtle
import math

def drawCircle(turtle_obj, center, radius):
    turtle_obj.penup()
    turtle_obj.goto(center[0], center[1] - radius)
    turtle_obj.pendown()
    distance = 2.0 * math.pi * radius / 120.0 
    for _ in range(120):
        turtle_obj.forward(distance)
        turtle_obj.right(3)

if __name__ == "__main__":
    screen = turtle.Screen()
    t = turtle.Turtle()
    x = float(input("Enter the x-coordinate of the circle's center: "))
    y = float(input("Enter the y-coordinate of the circle's center: "))
    radius = float(input("Enter the radius of the circle: "))

# Kock project
import turtle

def drawFractalLine(turtle_obj, length, level):
    if level == 0:
        turtle_obj.forward(length)
    else:
        segment_length = length / 3.0
        drawFractalLine(turtle_obj, segment_length, level - 1)
        turtle_obj.left(60)
        drawFractalLine(turtle_obj, segment_length, level - 1)
        turtle_obj.right(120)
        drawFractalLine(turtle_obj, segment_length, level - 1)
        turtle_obj.left(60)
        drawFractalLine(turtle_obj, segment_length, level - 1)

def drawKochSnowflake(turtle_obj, length, level):
    for _ in range(3):
        drawFractalLine(turtle_obj, length, level)
        turtle_obj.right(120)

if __name__ == "__main__":
    screen = turtle.Screen()
    t = turtle.Turtle()
    t.speed(0)
    level = int(input("Enter the level of the Koch snowflake (0, 1, or 2): "))
    length = float(input("Enter the length of each side of the snowflake: "))
    drawKochSnowflake(t, length, level)
    screen.mainloop()

# Speia project
image = Image("")
(red, green, blue) = image.getPixel(x,y)
if red < 63:
    red = int(red * 1.1)
    blue = int(blue * 0.9)
    elif red < 192:
        red = int(red * 1.15)
        blue = int(blue * 0.85)
    else:
        red = min(int(red * 1.08), 255)
        blue = int(blue * 0.93)

# Week ten code---------------------------------------------------------------------------------

# Taxformwithgui project
from breezypythongui import EasyFrame

class TaxCalculator(EasyFrame):
    def __init__(self):
        EasyFrame.__init__(self, title="Simple Tax Calculator")
        self.addLabel(text="Gross Income ($):", row=0, column=0)
        self.incomeField = self.addIntegerField(value=50000, row=0, column=1)
        self.addLabel(text="Number of Dependents:", row=1, column=0)
        self.dependentsField = self.addIntegerField(value=2, row=1, column=1)
        self.addLabel(text="Tax Owed ($):", row=2, column=0)
        self.taxOwedLabel = self.addLabel(text="$0.00", row=2, column=1)
        self.addButton(text="Compute", row=3, column=0, columnspan=2, command=self.compute_tax)
    def compute_tax(self):
        income = self.incomeField.getNumber()
        dependents = self.dependentsField.getNumber()
        dependent_deduction = 3000 * dependents
        taxable_income = income - dependent_deduction
        if taxable_income <= 0:
            tax_owed = 0
        elif taxable_income <= 9875:
            tax_owed = taxable_income * 0.10
        elif taxable_income <= 40125:
            tax_owed = 987.5 + (taxable_income - 9875) * 0.12
        elif taxable_income <= 85525:
            tax_owed = 4617.5 + (taxable_income - 40125) * 0.22
        elif taxable_income <= 163300:
            tax_owed = 14605.5 + (taxable_income - 85525) * 0.24
        else:
            tax_owed = 33271.5 + (taxable_income - 163300) * 0.32
        self.taxOwedLabel["text"] = f"${tax_owed:,.2f}"

if __name__ == "__main__":
    TaxCalculator().mainloop()
    
# Tempuraturewithgui project
from breezypythongui import EasyFrame
class TemperatureConverter(EasyFrame):
    def __init__(self):
        EasyFrame.__init__(self, title="Temperature Converter")
        self.addLabel(text="Fahrenheit:", row=0, column=0)
        self.fahrenheitField = self.addFloatField(value=32.0, row=1, column=0)
        self.addLabel(text="Celsius:", row=0, column=1)
        self.celsiusField = self.addFloatField(value=0.0, row=1, column=1)
        self.addButton(text=">>>>", row=2, column=0, command=self.fahrenheit_to_celsius)
        self.addButton(text="<<<<", row=2, column=1, command=self.celsius_to_fahrenheit)
    def fahrenheit_to_celsius(self):
        fahrenheit = self.fahrenheitField.getNumber()
        celsius = (fahrenheit - 32) * 5.0 / 9.0
        self.celsiusField.setNumber(celsius)
    def celsius_to_fahrenheit(self):
        celsius = self.celsiusField.getNumber()
        fahrenheit = celsius * 9.0 / 5.0 + 32
        self.fahrenheitField.setNumber(fahrenheit)

if __name__ == "__main__":
    TemperatureConverter().mainloop()




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

# Week five code---------------------------------------------------------------------------------

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

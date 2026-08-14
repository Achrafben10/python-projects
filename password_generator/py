# ==============================================
#           STRONG PASSWORD GENERATOR
# ==============================================

import random
import string


# Generate a password based on the user's requirements
def generate_password(length, upper_number, lower_number,
                      number_number, symbol_number):

    password = []

    # Add uppercase letters
    for i in range(upper_number):
        password.append(random.choice(string.ascii_uppercase))

    # Add lowercase letters
    for i in range(lower_number):
        password.append(random.choice(string.ascii_lowercase))

    # Add numbers
    for i in range(number_number):
        password.append(random.choice(string.digits))

    # Add symbols
    symbols = "!@#$%^&*()-_=+"

    for i in range(symbol_number):
        password.append(random.choice(symbols))

    # Fill the remaining characters
    all_characters = (
        string.ascii_letters
        + string.digits
        + symbols
    )

    remaining = length - len(password)

    for i in range(remaining):
        password.append(random.choice(all_characters))

    # Mix all characters
    random.shuffle(password)

    # Convert the list into one string
    return "".join(password)


# ==============================================
#                 MAIN PROGRAM
# ==============================================

print("==============================================")
print("          STRONG PASSWORD GENERATOR")
print("==============================================")
print()

# Ask the user for the password requirements
length = int(input("Password length: "))

upper_number = int(input("Number of uppercase letters: "))
lower_number = int(input("Number of lowercase letters: "))
number_number = int(input("Number of numbers: "))
symbol_number = int(input("Number of symbols: "))

# Check if the requirements fit the password length
required = (
    upper_number
    + lower_number
    + number_number
    + symbol_number
)

if required > length:

    print()
    print("Error: The requirements are longer")
    print("than the password length.")

else:

    # Generate the password
    password = generate_password(
        length,
        upper_number,
        lower_number,
        number_number,
        symbol_number
    )

    print()
    print("==============================================")
    print("             YOUR PASSWORD")
    print("==============================================")
    print()
    print(password)
    print()
    print("Password length:", len(password))
    print("==============================================")

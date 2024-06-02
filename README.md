import random
import string

def generate_password(length):
    # Define possible characters in the password
    characters = string.ascii_letters + string.digits + string.punctuation
    # Generate a random password
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    # Prompt user for the password length8
    while True:
        try:
            length = int(input("Enter the desired length for the password: "))
            if length <= 0:
                print("Please enter a positive number.")
            else:
                break
        except ValueError:
            print("Invalid input. Please enter a number.")

    # Generate the password
    password = generate_password(length)
    # Display the generated password
    print("Generated Password: ", password)

if _name_ == "main":
    main()

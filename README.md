import string
import random

def generate_random_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def generate_multiple_passwords(num_passwords=1, length=12):
    passwords = [generate_random_password(length) for _ in range(num_passwords)]
    return passwords

if __name__ == "__main__":
    try:
        length = int(input("Enter the length of the password(s): "))
        num_passwords = int(input("Enter the number of passwords to generate: "))
        generated_passwords = generate_multiple_passwords(num_passwords, length)
        
        print("\nGenerated Passwords:")
        for password in generated_passwords:
            print(password)
    except ValueError:
        print("Invalid input. Please enter valid numbers for length and number of passwords.")


        

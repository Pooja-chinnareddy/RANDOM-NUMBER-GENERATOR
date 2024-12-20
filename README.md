'''EXAMPLE OUTPUT:- Welcome to the Random Number Generator!
Enter the lower bound of the range: 1
Enter the upper bound of the range: 10
A random number between 1 and 10 is: 7
'''
# RANDOM-NUMBER-GENERATOR
import random

def random_number_generator():
    print("Welcome to the Random Number Generator!")
    
    # Get user input for the range
    try:
        lower_bound = int(input("Enter the lower bound of the range: "))
        upper_bound = int(input("Enter the upper bound of the range: "))
    except ValueError:
        print("Invalid input. Please enter integer values.")
        return
    
    if lower_bound > upper_bound:
        print("The lower bound must be less than or equal to the upper bound.")
        return
    
    # Generate a random number within the specified range
    random_number = random.randint(lower_bound, upper_bound)
    
    print(f"A random number between {lower_bound} and {upper_bound} is: {random_number}")

# Run the random number generator
if __name__ == "__main__":
    random_number_generator()

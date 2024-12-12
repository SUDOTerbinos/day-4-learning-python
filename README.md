# day-4-learning-python
it is day 4 to learn python i am not finished the code and if you see .py file i finished the code         here it is the link https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-regular-expressions-by-building-a-password-generator


    
     
     import re
     import secrets
     import string
    
    def generate_password(length, nums, special_chars, uppercase, lowercase):
      # Define the possible characters for the password
      letters = string.ascii_letters
      digits = string.digits
     symbols = string.punctuation

    # Combine all characters
    all_characters = letters + digits + symbols

    while True:
        password = ''
        # Generate password
        for _ in range(length):
            password += secrets.choice(all_characters)
        
        constraints = [
            (nums, r'\d'),
            (lowercase, r'[a-z]'),
            (uppercase, r'[A-Z]'),
            (special_chars, r'\W')
        ]        

    return password
    
    # new_password = generate_password(8)
    # print(new_password)   
    
    pattern = r'\W'
    quote = 'Not all those who wander are lost.'
    print(re.findall(pattern, quote))

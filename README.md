# The algorithm was tweaked to include punctuation in the translation. 

input = input().lower()


# List of letters
swap = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

# Makes a copy of the list of letters, and reverses the original copy.
other = swap.copy()
swap = swap[::-1]

letters = {}

# Combines both lists in a dictionary.
for i in range(26):
    x, y = swap[i], other[i]
    letters[y] = x

# Function to switch each letter in an array with it's pair in the dictionary "letters".
def switch(array):
    for i in range(len(array)):
        if array[i] == ' ' or array[i] not in swap:
            continue
        else:
            array[i] = letters[array[i]]

# Puts each letter of the user's input in a list so it can be switched.
input = [i for i in input]
    
# Calls on the function "switch".
switch(input)
    
# Converts the newly translated array back into a string.

print("".join(input))

    
          

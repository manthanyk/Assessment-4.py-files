# Assessment-4.py-files
 
Task 1: Read a File and Handle Errors

try:
    with open('sample.txt', 'r') as file:
        print("Reading file content:")
        for line in file:
            print(line.strip())  
except FileNotFoundError:
    print("Error: The file 'sample.txt' was not found.")
    
    Task 2: Write and Append Data to a File
 
user_input_write = input("Enter text to write to the file: ")
try:
    with open("output.txt", "w") as file:
        file.write(user_input_write + "\n")  # Add newline for better formatting
    print("Data successfully written to output.txt.")
except IOError:
    print("Error: Could not write to output.txt.")

user_input_append = input("Enter additional text to append: ")
try:
    with open("output.txt", "a") as file:
        file.write(user_input_append + "\n") # Add newline for better formatting
    print("Data successfully appended.")
except IOError:
    print("Error: Could not append to output.txt.")

print("\nFinal content of output.txt:")
try:
    with open("output.txt", "r") as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("Error: output.txt not found.")
except IOError:
    print("Error: Could not read from output.txt.") 

# handling-with-python-week5
handling with python week5 assignment

Demonstrate your understanding of Python file handling by completing the following tasks.

Tasks:

File Creation:
Create a Python script (file_handling_assignment.py) that does the following:
Creates a new text file named "my_file.txt" in write mode ('w').
Write at least three lines of text to the file, including a mix of strings and numbers.


File Reading and Display:
Enhance your script to read the contents of "my_file.txt" and display them on the console.


File Appending:
Modify the script to open "my_file.txt" in append mode ('a').
Append three additional lines of text to the existing content.


Error Handling:
Implement error handling using try, except, and finally blocks to manage potential file-related exceptions (e.g., FileNotFoundError, PermissionError).
# file_handling_assignment.py

def create_file():
    try:
        # File Creation
        with open('my_file.txt', 'w') as file:
            file.write("This is the first line of the file.\n")
            file.write("Here is the second line with a number: 123.\n")
            file.write("And this is the third line with some text.\n")
        print("File created and written successfully.")

    except (FileNotFoundError, PermissionError) as e:
        print(f"Error occurred while creating or writing to the file: {e}")
    finally:
        print("File creation process completed.")

def read_file():
    try:
        # File Reading and Display
        with open('my_file.txt', 'r') as file:
            contents = file.read()
            print("\nFile contents:")
            print(contents)
    
    except (FileNotFoundError, PermissionError) as e:
        print(f"Error occurred while reading the file: {e}")
    finally:
        print("File reading process completed.")

def append_to_file():
    try:
        # File Appending
        with open('my_file.txt', 'a') as file:
            file.write("Appending a new line to the file.\n")
            file.write("Another new line added.\n")
            file.write("Final new line appended.\n")
        print("File appended successfully.")

    except (FileNotFoundError, PermissionError) as e:
        print(f"Error occurred while appending to the file: {e}")
    finally:
        print("File appending process completed.")

if __name__ == "__main__":
    create_file()
    read_file()
    append_to_file()
    read_file()  # Read the file again to display the appended content
python file_handling_assignment.py

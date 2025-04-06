# Week-4-assignment
File Read & Write Challenge 🖋️: Create a program that reads a file and writes a modified version to a new file.
Error Handling Lab 🧪: Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.


def main():
    # File names
    input_file = "example.txt"
    output_file = "modified_example.txt"

    try:
        # Open and read the original file
        with open(input_file, "r") as file:
            content = file.read()

        # Modify the content (make it uppercase)
        modified_content = content.upper()

        # Write the modified content to a new file
        with open(output_file, "w") as file:
            file.write(modified_content)

        print(f"Content was successfully written to '{output_file}'.")

    except FileNotFoundError:
        print(f"The file '{input_file}' was not found.")
    except Exception as e:
        print(f"Something went wrong: {e}")
main()

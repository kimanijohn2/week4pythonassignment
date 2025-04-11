# week4pythonassignment
def read_and_write_file(input_filename, output_filename):
    try:
        with open(input_filename, "r") as input_file:
            content = input_file.read()
        with open(output_filename, "w") as output_file:
            output_file.write(content)
        print("File read and written successfully.")
    except FileNotFoundError:
        print("File not found.")
    except Exception as e:
        print("An error occurred while reading or writing the file:", e)
input_filename = input("Enter the input filename: ")
output_filename = input("Enter the output filename: ")

try:
    with open(input_filename, "r") as input_file:
        content = input_file.read()
except FileNotFoundError:
    print("File not found.")
    exit()

with open(output_filename, "w") as output_file:
    output_file.write(content)

print("File read and written successfully.")

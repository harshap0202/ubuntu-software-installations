# Basic Shell Scripting Commands

## Creating and Editing Scripts

```bash
# Create a new shell script file
nano script.sh

# Make the script executable
chmod +x script.sh

# Run the script
./script.sh
```

## Basic Script Structure

```bash
#!/bin/bash
# Comment

# Print a message to the terminal
echo "Hello, World!"

# Variables
TEST_VAR="Hello"
echo $TEST_VAR

# Command substitution
current_date=$(date)
echo "Current date: $current_date"
```

## Conditional Statements

```bash
#!/bin/bash

# If-else statement
if [ "$my_var" == "Hello" ]; then
    echo "The variable is Hello"
else
    echo "The variable is not Hello"
fi

# Case statement
case $my_var in
    "Hello")
        echo "Greeting detected"
        ;;
    *)
        echo "Unknown value"
        ;;
esac
```

## Loops

```bash
#!/bin/bash

# For loop
for i in {1..5}; do
    echo "Number $i"
done

# While loop
counter=1
while [ $counter -le 5 ]; do
    echo "Counter $counter"
    ((counter++))
done

# Until loop
counter=1
until [ $counter -gt 5 ]; do
    echo "Counter $counter"
    ((counter++))
done
```

## Functions

```bash
#!/bin/bash

# Define a function
greet() {
    local name=$1
    echo "Hello, $name!"
}

# Call the function
greet "World"
```

## File and Directory Operations

```bash
#!/bin/bash

# Create a directory
mkdir my_directory

# Change to the directory
cd my_directory

# Create a file
touch my_file.txt

# List files
ls

# Remove a file
rm my_file.txt

# Remove a directory (if empty)
rmdir my_directory

# Remove a directory (with contents)
rm -r my_directory
```

## Read Input and Get Output

```bash
#!/bin/bash

# Read user input
read -p "Enter your name: " user_name
echo "Hello, $user_name!"

# Redirect output to a file
echo "This is a test" > test.txt

# Append output to a file
echo "Additional text" >> test.txt

# Read from a file
while IFS= read -r line; do
    echo "$line"
done < test.txt
```

## Error Handling and Debugging

```bash
#!/bin/bash -evx

# -e to exit on error
# -v to get verbose output
# -x to see executions

```

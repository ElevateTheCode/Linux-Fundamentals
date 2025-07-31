Part 1: The Basics
This is where you start. Every Bash script begins with these core elements.

Shebang: The very first line of any script must be #!/bin/bash. This tells the operating system to use the Bash shell to execute the script.

Comments: Use the # symbol to add comments. Comments are ignored by the shell and are for human readers.

Bash

# This is a comment, it explains the script's purpose.
echo "Hello, World!" # This is also a comment.
Variables: You can store values in variables. Variable names are typically uppercase.

Bash

MY_NAME="Alice"
echo "My name is $MY_NAME."
Executing a Script:

Save your code in a file (e.g., myscript.sh).

Make the file executable: chmod +x myscript.sh.

Run the script: ./myscript.sh.
---

Part 2: Working with Commands and Input
Bash is all about running commands. These techniques allow you to make your scripts interactive and powerful.

Command Output: The output of a command can be captured into a variable using command substitution.

Bash

CURRENT_DATE=$(date)
echo "Today's date is: $CURRENT_DATE"
Input from User: The read command prompts the user for input and stores it in a variable.

Bash

echo "What is your name?"
read USER_NAME
echo "Hello, $USER_NAME!"
Command Line Arguments: Your script can accept arguments from the command line.

Bash

# Run the script like this: ./myscript.sh file1.txt
echo "The first argument is: $1"
echo "The script name is: $0"
echo "All arguments are: $@"
---
Part 3: Control Flow and Logic
Control flow allows your script to make decisions and repeat actions.

If/Else Statements: Run a block of code only if a certain condition is met.

Bash

if [ "$1" == "start" ]; then
    echo "Starting the service..."
elif [ "$1" == "stop" ]; then
    echo "Stopping the service..."
else
    echo "Usage: ./myscript.sh [start|stop]"
fi
Note: The spaces around the [ and ] are required.

Comparison Operators: Used inside if statements to compare values.

== or != for strings.

-eq, -ne, -gt, -lt, -ge, -le for integers (equals, not equals, greater than, etc.).

For Loops: Repeat a set of commands for each item in a list.

Bash

for file in *.txt; do
    echo "Processing $file"
done
While Loops: Repeat a block of code as long as a condition is true.

Bash

COUNT=1
while [ $COUNT -le 5 ]; do
    echo "Count: $COUNT"
    COUNT=$((COUNT + 1))
done
---

Part 4: Functions and Script Organization
As your scripts grow, functions help you keep your code clean and reusable.

Functions: A way to group a series of commands and give them a name.

Bash

function greet() {
    echo "Hello, $1!"
}
# Call the function
greet "World"
Case Statements: A cleaner alternative to a long if/elif/else chain for matching different values.

Bash

case "$1" in
    "start")
        echo "Starting..."
        ;;
    "stop")
        echo "Stopping..."
        ;;
    *) # Default case
        echo "Invalid command."
        ;;
esac
Handling Errors: Use set -e at the top of your script to make it exit immediately if any command fails. This prevents a script from continuing to run with a bad state.

This guide provides a solid foundation. To truly master Bash scripting, you must practice and experiment with these concepts. Start with simple scripts and gradually build up to more complex ones that solve your daily automation needs.

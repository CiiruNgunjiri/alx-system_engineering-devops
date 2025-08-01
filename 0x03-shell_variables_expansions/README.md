# 0x03 Shell Variables and Expansions

This project contains a series of small bash scripts designed to practice and demonstrate knowledge of shell variables, environment variables, expansions, shell arithmetic, aliases, and shell scripting fundamentals. Each script is exactly two lines long, executable, and targets Ubuntu 20.04 LTS.

## Files and Descriptions

### 0-alias  
Creates an alias `ls` that runs `rm *`, effectively removing all files in the current directory when `ls` is called. Use `\ls` to bypass the alias.

### 1-hello_you  
Prints `hello` followed by the current Linux username using the `$USER` environment variable.

### 2-path  
Appends `/action` directory to the end of the existing `PATH` environment variable, to be searched last for executable files.

### 4-global_variables  
Prints all environment (global) variables using the `printenv` command.

### 5-local_variables  
Lists all local variables, environment variables, and shell functions visible in the current shell using `declare -p`.

### 6-create_local_variable  
Creates a local variable `BEST` with the value `School`. The variable is available only within the current shell or script.

### 7-create_global_variable  
Creates and exports a global environment variable `BEST=School`, available in child processes after sourcing the script.

### 8-true_knowledge  
Prints the result of adding 128 to the environment variable `TRUEKNOWLEDGE`.

### 9-divide_and_rule  
Prints the integer result of dividing the environment variable `POWER` by `DIVIDE`.

### 10-love_exponent_breath  
Prints the result of raising the variable `BREATH` to the power of `LOVE`.

### 11-binary_to_decimal  
Converts a binary number stored in the environment variable `BINARY` to its decimal equivalent.

### 12-combinations  
Prints all possible two-letter lowercase combinations from `aa` to `zz`, excluding `oo`. The output is alphabetically sorted, one per line.

### 13-print_float  
Prints the value of the environment variable `NUM` formatted to two decimal places.

## Requirements and Constraints

- All scripts include the shebang `#!/bin/bash` as the first line.
- Scripts are exactly 2 lines long; the second line contains the main logic.
- No use of `&&`, `||`, or `;` to combine commands.
- Avoid using external utilities like `bc`, `sed`, or `awk` unless explicitly allowed.
- Must be executable (`chmod +x <script>`).
- Tested on Ubuntu 20.04 LTS.
- Ends with a newline character.

## Usage Instructions

Generally:

1. Clone or download this repository.
2. Navigate to `0x03-shell_variables_expansions`.
3. Make sure each script you want to run is executable, e.g.,  
   `chmod +x <script_name>`
4. Export required environment variables before running scripts that depend on them.  
   Example:  
export TRUEKNOWLEDGE=1209
./8-true_knowledge

text
5. For scripts that create or update variables or aliases, source them in the current shell to preserve the environment changes, e.g.,  
source ./2-path
echo $PATH

text

## Author

ciiru_ngunjiri

---

Feel free to ask if you want help updating or extending this README!
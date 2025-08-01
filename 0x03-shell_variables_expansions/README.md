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

### 100-decimal_to_hexadecimal
Description: Converts a decimal (base 10) number stored in the environment variable DECIMAL to its hexadecimal (base 16) lowercase representation.

Implementation: Uses Bash built-in printf for conversion.

Usage:

bash
export DECIMAL=1337
./100-decimal_to_hexadecimal
# Output: 539

###  101-rot13
Description: Reads input from standard input and outputs the ROT13-encoded text.

Implementation: Utilizes tr for ASCII text character substitution.

Usage:

bash
./101-rot13 < inputfile

### 102-odd
Description: Prints every other line from input, starting with the first line.

Implementation: Uses awk with condition on record number.

Usage:

bash
ls -1 | ./102-odd

### 103-water_and_stir
Description: Adds two numbers given in non-standard bases:

WATER is a number in base "water" (w,a,t,e,r).

STIR is a number in base "stir" (s,t,i,r).

Outputs the sum in base "bestchol" (b,e,s,t,c,h,o,l).

Constraints:

No use of &&, ||, ;, sed, or bc.

Pure Bash with built-in arithmetic.

Strict checking of digit validity.

Provided as a strictly 2-line script using embedded multi-line logic via bash -c.

Important:

The input variables must only contain valid characters from their respective digit sets.

Invalid characters (e.g., . in STIR) will cause the script to error out.

Usage:

bash
export WATER="ewwatratewa"
export STIR="tiitirtrtr"  # Ensure only valid digits present
./103-water_and_stir

## General Notes
All scripts are designed to be portable and conform to strict shell scripting standards suitable for system engineering tasks.

Explicitly avoid forbidden operators to ensure simple, maintainable, and portable shell code.

Use executable permissions where necessary:

bash
chmod +x script_name
Input validation is performed where applicable to ensure meaningful error messages.

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
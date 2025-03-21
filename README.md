# linuxadminstraion
#!/bin/bash

# 1. System Information Script
echo "System Information:" > system_info.txt
echo "-------------------" >> system_info.txt

echo "Hostname: $(hostname)" >> system_info.txt
echo "OS: $(uname -o)" >> system_info.txt
echo "Kernel Version: $(uname -r)" >> system_info.txt
echo "CPU Info: $(lscpu | grep 'Model name')" >> system_info.txt
echo "Total Memory: $(free -h | grep 'Mem:' | awk '{print $2}')" >> system_info.txt
echo "Disk Usage: $(df -h / | tail -1 | awk '{print $3 "/" $2}')" >> system_info.txt
echo "System info saved to 'system_info.txt'"

# 2. Basic Mathematical Calculation Script
echo "Enter first number: "
read num1
echo "Enter second number: "
read num2

sum=$((num1 + num2))
diff=$((num1 - num2))
product=$((num1 * num2))
quotient=$((num1 / num2))

# Redirecting output to a file
echo "Mathematical Calculations:" > calculations.txt
echo "-------------------------" >> calculations.txt
echo "Sum: $sum" >> calculations.txt
echo "Difference: $diff" >> calculations.txt
echo "Product: $product" >> calculations.txt
echo "Quotient: $quotient" >> calculations.txt
echo "Calculations saved to 'calculations.txt'"

# 3. Using Redirection Operators
echo "Listing files in current directory..." > output.txt
ls -l >> output.txt
echo "Files listed in 'output.txt'" 12345

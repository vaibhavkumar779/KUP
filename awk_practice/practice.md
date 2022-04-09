## commands

print every line of a specified file

awk '{print}' employee.txt

print matching word line in a file

awk '/engineer/ {print}' employee.txt

print paticular column in a file

awk '{print $1 $4}' employee.txt

$0 prints whole line

print line number use NR

awk '{print NR,$0}' employee.txt
# Table of Contents

1. [Code for Drawing](#code-for-drawing)
2. [Find HCF](#find-hcf)
3. [Bubble Sort (Ascending)](#Bubble-sort (ASCENDING))
4. [Bubble Sort in Python (AI Teach)](#bubble-sort-in-python-ai-teach)

# code for drawing
```
def initialize_display():
# Define the bit pattern for an 4x4 display
  bit_pattern = "1111100110011111"
  # Initialize an 4x4 display list
  display = []
  # Populate the display with the bit pattern
  for i in range(4):  # 4 rows
    row = []
    for j in range(4):  # 4 columns
      # Convert each bit into an integer and add to the row
      row.append(int(bit_pattern[i * 4 + j]))
    display.append(row)
  return display

def print_display(display):
  # Print the display in a format that represents an LED panel
  #for row in display:
  #  print(' '.join(['*' if bit else ' ' for bit in row]))
  for row in display:
    display_text=""
    for bit in row:
      if bit == 1:
        display_text=display_text+"* "
      else:
        display_text=display_text+"  "
    print(display_text)
def main():
  display = initialize_display()
  print_display(display)

main()
```

# Find HCF
```
def func(a, b):
    k = min(a, b)  # Using min() instead of minimum()
    y = 1  # Initialize y
    for i in range(1, k + 1):
        if a % i == 0 and b % i == 0:  # Fixed the condition (was a%1)
            y = i
    return y

# Test the function
a = 6
b = 9
result = func(a, b)
print(result)
```
# Bubble sort
[click here](https://github.com/hugow0528/w_progland/blob/8e0249f6d53b35f199b00bb7182ea1fc2a22cd02/bubble%20sort%20.md)
# fibonacci
[click here](https://github.com/hugow0528/w_progland/blob/8e0249f6d53b35f199b00bb7182ea1fc2a22cd02/fibonacci.md)

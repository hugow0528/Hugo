# Table of Contents

1. [Code for Drawing](#code-for-drawing)
2. [Find HCF](#find-hcf)
3. [Bubble Sort (Ascending)](#bubble-sort-ascending)
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

# Bubble sort (ASSCENDING)
E.G.1:<BR>unsorted=[1,4,2,3] <BR>
1st pass : 1,4,2,3 <BR>
2nd pass : 1,2,4,3 <BR>
3nd pass : 1,2,3,4 <BR>

```
def bubble_sorted(iterable):
    new_list = list(iterable)
    list_len = len(new_list)
    for i in range(list_len-1):
        for j in range(list_len - i - 1):
            if new_list[j] > new_list[j + 1]:
                new_list[j], new_list[j + 1] = new_list[j + 1], new_list[j]
    return new_list

```
<BR>
unsorted=[2,4,1,3]<br>
1st place: 2,4,1,3<br>
2,4,1,3<br>
2,1,4,3<br>
2,1,3,4<br>

# Bubble Sort in Python (ai teach)

Bubble Sort is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.

## How Bubble Sort Works

1. Start at the beginning of the list.
2. Compare the first two adjacent elements.
3. If the first element is greater than the second, swap them.
4. Move to the next pair of adjacent elements and repeat the process.
5. Continue this until the end of the list is reached.
6. Repeat the entire process for the list until no swaps are needed, indicating that the list is sorted.

## Python Implementation

Here is a simple implementation of Bubble Sort in Python:

```python
def bubble_sort(arr):
    n = len(arr)
    # Traverse through all array elements
    for i in range(n):
        # Last i elements are already in place
        for j in range(0, n-i-1):
            # Traverse the array from 0 to n-i-1
            # Swap if the element found is greater
            # than the next element
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

# Example usage
arr = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(arr)
print("Sorted array:", arr)

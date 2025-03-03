# hi
This is the place that I will show my program 

# Digital Clock with Timer and Stopwatch
You can view the digital clock with timer and stopwatch [here](https://github.com/hugow0528/w_progland/blob/main/index%20(1).html).


# code for draw
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

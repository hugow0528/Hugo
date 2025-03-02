# hi
[anaconda](https://anaconda.cloud/)

# code for draw
`def initialize_display():
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
`

```
def fibonacci_iterative(n):
  if n <= 0:
    return []
  elif n == 1:
    return [0]
  elif n == 2:
    return [0, 1]

  fib_sequence = [0, 1]
  for i in range(2, n):
    next_fib = fib_sequence[-1] + fib_sequence[-2]
    fib_sequence.append(next_fib)
  return fib_sequence

def main():
  n = int(input("Enter the number of Fibonacci numbers to generate: "))
  result = fibonacci_iterative(n)
  print("Fibonacci sequence (iterative):")
  print(result)

if __name__ == "__main__":
    main()
```
Enter the number of Fibonacci numbers to generate: 10 <BR>
Fibonacci sequence (iterative):<BR>
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]<BR>


<br><br>
```
def fibonacci_recursive(n):
  if n <= 0:
    return []
  elif n == 1:
    return [0]
  elif n == 2:
    return [0, 1]
  else:
    fib_sequence = fibonacci_recursive(n-1)
    next_fib = fib_sequence[-1] + fib_sequence[-2]
    fib_sequence.append(next_fib)
    return fib_sequence

def main():
  n = int(input("Enter the number of Fibonacci numbers to generate: "))
  result = fibonacci_recursive(n)
  print("Fibonacci sequence (recursive):")
  print(result)

if __name__ == "__main__":
  main()
```
Enter the number of Fibonacci numbers to generate: 5<BR>
Fibonacci sequence (recursive):<BR>
[0, 1, 1, 2, 3]<BR>

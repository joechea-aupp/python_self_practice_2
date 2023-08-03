Exercise 1: Print a Multiplication Table
```python
def multiplication_table(number):
    for i in range(1, 11):
        print(f"{number} x {i} = {number * i}")

# Example usage
multiplication_table(5)
```

Exercise 2: Find the Largest Number in a List
```python
def find_largest_number(numbers):
    largest = numbers[0]
    for num in numbers:
        if num > largest:
            largest = num
    return largest

# Example usage
numbers = [23, 45, 12, 67, 34, 89]
print(find_largest_number(numbers))
```

Exercise 3: Reverse a String
```python
def reverse_string(input_string):
    reversed_string = ""
    for char in input_string:
        reversed_string = char + reversed_string
    return reversed_string

# Example usage
input_string = "hello"
print(reverse_string(input_string))
```

Exercise 4: Calculate the Sum of a 2D List
```python
def calculate_2d_list_sum(matrix):
    total_sum = 0
    for row in matrix:
        for num in row:
            total_sum += num
    return total_sum

# Example usage
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(calculate_2d_list_sum(matrix))
```

Exercise 5: Implement a Stack using a Python Class
```python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        return None

    def is_empty(self):
        return len(self.items) == 0

# Example usage
stack = Stack()
stack.push(5)
stack.push(10)
print(stack.pop())
print(stack.is_empty())
```

Exercise 6: Check for Palindrome
```python
def is_palindrome(input_string):
    return input_string == input_string[::-1]

# Example usage
string1 = "radar"
string2 = "hello"
print(is_palindrome(string1))
print(is_palindrome(string2))
```

Exercise 7: Prime Numbers in a Range
```python
def is_prime(number):
    if number <= 1:
        return False
    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            return False
    return True

def find_primes_in_range(start, end):
    primes = []
    for num in range(start, end + 1):
        if is_prime(num):
            primes.append(num)
    return primes

# Example usage
start = 10
end = 50
print(find_primes_in_range(start, end))
```

Exercise 8: Fibonacci Sequence
```python
def fibonacci_sequence(n):
    fib_sequence = [0, 1]
    for i in range(2, n):
        fib_sequence.append(fib_sequence[-1] + fib_sequence[-2])
    return fib_sequence

# Example usage
n = 10
print(fibonacci_sequence(n))
```

Exercise 9: Find Common Elements in Lists
```python
def find_common_elements(list1, list2):
    common_elements = []
    for element in list1:
        if element in list2 and element not in common_elements:
            common_elements.append(element)
    return common_elements

# Example usage
list1 = [1, 2, 3, 4, 5]
list2 = [3, 4, 5, 6, 7]
print(find_common_elements(list1, list2))
```

Exercise 10: Tic-Tac-Toe Game
```python
class TicTacToe:
    def __init__(self):
        self.board = [[' ' for _ in range(3)] for _ in range(3)]
        self.current_player = 'X'

    def make_move(self, row, col):
        if 0 <= row < 3 and 0 <= col < 3 and self.board[row][col] == ' ':
            self.board[row][col] = self.current_player
            self.current_player = 'O' if self.current_player == 'X' else 'X'

    def check_win(self):
        # Check rows, columns, and diagonals for a win
        for i in range(3):
            if self.board[i][0] == self.board[i][1] == self.board[i][2] != ' ':
                return True
            if self.board[0][i] == self.board[1][i] == self.board[2][i] != ' ':
                return True
        if self.board[0][0] == self.board[1][1] == self.board[2][2] != ' ':
            return True
        if self.board[0][2] == self.board[1][1] == self.board[2][0] != ' ':
            return True
        return False

    def display_board(self):
        for row in self.board:
            print(' | '.join(row))
            print('-' * 5)

# Example usage
game = TicTacToe()
game.make_move(0, 0)
game.make_move(1, 1)
game.make_move(0, 1)
game.make_move(2, 2)
game.make_move(0, 2)
game.display_board()
print(game.check_win())
```

Please note that these are just one way to solve each problem. There can be various approaches to tackle these exercises. Happy coding and learning!

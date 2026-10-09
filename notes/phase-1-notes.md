# Python
## Errors and Exceptions :
- Errors are usually synthax errors in python a missing ":" in a loop or a forgotten array in a dictionary or even a mistyped function, Python points on the terminal so you don't have to search by yourself.
- Excpetions on the other hand are more subtle, even if the synthax is correct it can throw an error message the most obvious one is the Dvision by zero or concatenating a string with a number or a unassigned variable.
## Handling Exceptions :
However you can control the output of the Exception it is called handling with a try/except statements
```python
while True:
    try:
        x = int(input("Enter a number"))
        break
    except ValueError:
        print("Invalid number, Please try again")
```
In the example above, we are asking for the user to choose any given integer number, if it's the case then the loop stops and move to the following instruction or code that you have written. However, if it's not the case then it moves to the except clause and prints the message, this will persist and display the message everytime the user enter an invalid number.  

If it doesn't match the exception named in the expect clause in our case "ValueError" then it passes tp the try statement.  

If there's no handlers found it throws an error message. 

It is better to avoid bare except because it catches evrery bug even the one you'd want to see.
```python
except: #bad

except(ValueError,ZeroDivisionError,Exception): # better and we packed it on a tuple instead of a chain of excepts, if that was the case it would be checked from top to bottom and if something matches it prints the error and exit
```  
  
A more efficient way to display an error message is to assign to a variable.  

  
```python
try:
    open("missing.txt")
except FileNotFoundError as e:
    print("Problem:", e)
```




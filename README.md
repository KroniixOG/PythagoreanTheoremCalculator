# PythagoreanTheoremCalculator
import math

while True:
    var = input("Which variable are you looking for (a, b, or c)? ")
    if var.lower() == "c":
        a = float(input("a: "))
        b = float(input("b: "))
        result = math.sqrt(a**2 + b**2)
        result = int(result) if result.is_integer() else result
        print("c:", result, "\n")
    elif var.lower() == "a":
        b = float(input("b: "))
        c = float(input("c: "))
        if c < b:
            print("MATH ERROR!! B cannot be greater than C""\n")
        else:
            result = math.sqrt(c**2 - b**2)
            result = int(result) if result.is_integer() else result
            print("a:", str(result), "\n")
    elif var.lower() == "b":
        a = float(input("a: "))
        c = float(input("c: "))
        if c < a:
            print("MATH ERROR!! A cannot be greater than C", "\n")
        else:
            result = math.sqrt(c**2 - a**2)
            result = int(result) if result.is_integer() else result
            print("b:", str(result), "\n")
    else:
        print("Uh oh, that's not an option buddy!", "\n")

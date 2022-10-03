---
title: Hex to number
tags: math
expertise: beginner
firstSeen: 2022-10-02T05:00:00-04:00
---

Explain briefly what the snippet does.
Returns the decimal representation of the a hexadecimal number.
- Explain briefly how the snippet works.
- Use `hex_to_int()` to convert a given Hexadecimal number into its decimal equivalent.

```py
def hex_to_int(hex):
    #taking the input for the hexa decimal number
    k = 0
    numVal = i = 0
    size = len(hex) - 1
    #I am calculating the max power value inside the variable named size.
    while size>=0:
        if  hex[size]>='A' and hex[size]<='F':
            rem = ord(hex[size]) - 55
            #Basically I used an ord func as it accepts a string of unit length as an argument and returns the Unicode equivalence of the passed argument.
            #Based on that I subtracted.
        elif hex[size]>='0' and hex[size]<='9':
            rem = int(hex[size])
        elif hex[size]>='a' and hex[size]<='f':
            rem = ord(hex[size]) - 87
        else:
            k = 1
            break
        numVal = numVal + (rem * (16 ** i))
        size = size - 1
        i = i+1    
    return print(numVal)
hex = input()
#taking the input for the hexa decimal number
hex_to_int(hex)
```

```py
hex_to_int(10) # 16
hex_to_int(f) # 15
```

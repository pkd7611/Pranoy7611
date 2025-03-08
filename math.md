
# Base Conversion 
# Base 11 to Base 10 for 343

def base_conv(n,b):
    s = str(n)
    length = len(s) # size of the input number
    output = 0
    last_digit = n%10 # to get the last digit(10**0 unit)
    prev_last = n//10 # to get the last-1 digit(10**1 unit)
    first_digit = n//100 # to get the first digit(10**2 unit)
    for i in range(length):
        digit = int(s[i])
        power = length-1-i
        output = output + digit*(b**power)
    return output

base_conv(343,11) -> 410

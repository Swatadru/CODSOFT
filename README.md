# CODSOFT
#Simple Calculator
#SP_PROFESSIONAL
def calc(num1,num2,opp):
    if opp == "+":
        result = num1 + num2
    elif opp == "-":
        result = num1-num2
    elif opp == "*":
        result = num1*num2
    elif opp == " / ":
        result = num1/num2
    else:
        print("Invalid operation",opp)
    return result
s = input("Enter the operation : ")
a = float(input("Enter 1st number : "))
b = float(input("Enter 2nd number : "))
print(calc(a,b,s))

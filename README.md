# MyCaculator
import math
print("-------------welcome to my calculator------------")
print("                Select Operation                ")
print("1  Add:")
print("2  Sub:")
print("3  Mul:")
print("4  div:")
print("5  sqrt:")
print("6  sin:")
print("7  cos:")
print("8  tan:")
print("9  cot:")
print("10 factorial:")
A= input("please enter 1 to 10 for more:")

if A in ("1","2","3","4"):
    number1= float(input("please enter the first number:"))
    number2= float(input("please enter the second number:"))
    if A=="1":
        print("Result:",number1+number2)
    elif A=="2":
        print("Result:",number1-number2)
    elif A=="3":
        print("Result:",number1*number2)
    elif A=="4":
        if number2==0:
            print("can't dvide by zero")
        else:
            print("Result:",number1/number2)
elif A in ("5","6","7","8","9","10"):
    number3=float(input("please enter a number:"))
    radian=number3*(math.pi/180)
    if A=="5":
        if number3<0:
            input("please inter a valid number again:")
        else:
            print("Result:",math.sqrt(number3))
    elif A=="6":
        print(math.sin(radian))
    elif A=="7":
        print(math.cos(radian))
    elif A=="8":
        print(math.tan(radian)) 
    elif A=="9":
        cot=1/(math.tan(radian))
        print("result:",cot)
    elif A=="10":
        if number3 < 0:
            print("invalid number!!!")
        elif number3 == 0:
            print("Result :1")
        else:
            result=1
            for i in range(1,int(number3)+1):
                result *=i
            print("Result:",result) 
else:
    print("invalid input")


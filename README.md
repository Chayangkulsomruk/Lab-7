def InsertionSortFunction(Ans):
    for i in range(1, len(Ans)):
        Ans1 = Ans[i]
        L = i-1
        while L >=0 and Ans1 < Ans[L] :
                Ans[L+1] = Ans[L]
                L -= 1
        Ans[L+1] = Ans1

def SelectionSortFunction(Ans):
    AllDATA = len(Ans)
    for Ans2 in range(AllDATA):
        center = Ans2
        for L in range(Ans2 + 1, AllDATA):
            if Ans[L] < Ans[center]:
                center = L
        (Ans[Ans2], Ans[center]) = (Ans[center], Ans[Ans2])

def BubbleSortFunction(Ans):
    T = len(Ans)
    Ans3 = False
    for i in range(T-1):
        for L in range(0, T-i-1):
            if Ans[L] > Ans[L + 1]:
                Ans3 = True
                Ans[L], Ans[L + 1] = Ans[L + 1], Ans[L]
        if not Ans3:
            return

print("All Sort Option You have")
print(" 1.| BubbleSortFunction   |\n 2.| SelectionSortFunction|\n 3.| InsertionSortFunction|")
print("****************************")

data = [11, 4, 7, 5, 10, 9, 13, 1]
mytext = "AllData"
x = mytext.center(28,"-")
print(x) 

for i in range(len(data)):
    print("% d" % data[i], end=" ")
print("\n----------------------------")    
print("****************************")
reply =int(input("please select sort option 1-3 : "))

Userinput = False
if reply == 1:
    BubbleSortFunction(data)
elif reply == 2:
    SelectionSortFunction(data)
elif reply == 3:
    InsertionSortFunction(data)
else:
    Userinput = True
    mytext3 = "please select number 1-3"
    x = mytext3.center(28,"*")
    print(x)
    print("\n----------------------------")

if not Userinput:
    mytext2 = "Your Answer is"
    x = mytext2.center(28,"-")
    print(x)
    for i in range(len(data)):
        print("% d" % data[i], end=" ")
    print("\n----------------------------")

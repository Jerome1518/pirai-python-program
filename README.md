n = int(input("Enter the limit:"))
i = 0
j = 1


def condition(choice):
    i = 0
    if (choice == 1):
        f = input("Enter the Author Name:")
        if f in dictA.values():
            print(dictA)
            i += 1
        if f in dictB.values():
            print(dictB)
            i += 1
        if f in dictC.values():
            print(dictC)
            i += 1
        if (i == 0):
            i = 0
            print("No Books available")
    if (choice == 2):
        if choice == 2:
            a = dictA["Book_cost"]
            b = dictB["Book_cost"]
            c = dictC["Book_cost"]
            if (a > b) and (a > c):
                print("a1:" + a)
                if (b > c):
                    print("b1:" + b)
                    print(dictC)
                    print(dictB)
                    print(dictA)
                else:
                    print("c1:" + c)
                    print(dictB)
                    print(dictC)
                    print(dictA)
            elif (b > a) and (b > c):
                print("b2:" + b)
                if (a > c):
                    print("a2:" + a)
                    print(dictC)
                    print(dictA)
                    print(dictB)
                else:
                    print("c2:" + c)
                    print(dictA)
                    print(dictC)
                    print(dictB)
            elif (c > a) and (c > b):
                print("c3:" + c)
                if (a > b):
                    print("a3:" + a)
                    print(dictB)
                    print(dictA)
                    print(dictC)
                else:
                    print("b3:" + b)
                    print(dictA)
                    print(dictB)
                    print(dictC)
    if (choice == 3):
        i = 0
        a = dictA["Pub_year"]
        b = dictB["Pub_year"]
        c = dictC["Pub_year"]
        f = input("Enter The Author Name:")
        y = input("Enter The Publishing Year:")
        if f in dictA.values():
            if y == a:
                print(dictA)
                i += 1
        if f in dictB.values():
            if y == b:
                print(dictB)
                i += 1
        if f in dictC.values():
            if y == c:
                print(dictC)
                i += 1
        if i == 0:
            i = 0
            print("No Books available")
    if choice == 4:
        f = input("Enter the Author Name:")
        if dictA["Pub_year"] > dictB["Pub_year"]:
            if dictB["Pub_year"] > dictC["Pub_year"]:
                if f in dictC.values():
                    print(dictC)
                if f in dictB.values():
                    print(dictB)
                if f in dictA.values():
                    print(dictA)
            elif dictA["Pub_year"] > dictC["Pub_year"]:
                if f in dictB.values():
                    print(dictB)
                if f in dictC.values():
                    print(dictC)
                if f in dictA.values():
                    print(dictA)
            else:
                if f in dictB.values():
                    print(dictB)
                if f in dictA.values():
                    print(dictA)
                if f in dictC.values():
                    print(dictC)

        elif dictB["Pub_year"] > dictC["Pub_year"]:
            if dictA["Pub_year"] > dictC["Pub_year"]:
                if f in dictC.values():
                    print(dictC)
                if f in dictA.values():
                    print(dictA)
                if f in dictB.values():
                    print(dictB)
            elif dictA["Pub_year"] > dictB["Pub_year"]:
                if f in dictA.values():
                    print(dictA)
                if f in dictC.values():
                    print(dictC)
                if f in dictB.values():
                    print(dictB)
            else:
                if f in dictA.values():
                    print(dictA)
                if f in dictB.values():
                    print(dictB)
                if f in dictC.values():
                    print(dictC)

    if choice == 5:
        exit()


for i in range(0, n):
    Author_name = input("Enter The Author_name:")
    Book_name = input("Enter The Book_name:")
    Book_version = input("Enter The Book_version:")
    Pub_year = input("Enter The Pub_year:")
    Book_cost = input("Enter The Book_cost in same digits:")
    add = int(input("Enter the dict number:"));
    if (add == 1):
        dictA = {"Author_name": Author_name, "Book_name": Book_name, "Book_version": Book_version, "Pub_year": Pub_year,
                 "Book_cost": Book_cost}
    elif (add == 2):
        dictB = {"Author_name": Author_name, "Book_name": Book_name, "Book_version": Book_version, "Pub_year": Pub_year,
                 "Book_cost": Book_cost}
    elif (add == 3):
        dictC = {"Author_name": Author_name, "Book_name": Book_name, "Book_version": Book_version, "Pub_year": Pub_year,
                 "Book_cost": Book_cost}

print(
    "1. Enter Author Name\n2. Enter Price\n3. Enter Author Name and Year of Publishing\n4.Enter Author Name,Publishing Year for listing\n5.To Exit")
while j == 1:
    choice = int(input("Enter the choice:"))
    condition(choice)

#Intro
name = input("Enter Student Name : ")
print(f"Welcome To Python Tutorial System {name}!")
print(""*50)

while True:
    #Board
    print("="*30)
    print("PYTHON TUTORIAL SYSTEM")
    print("="*30)
    print("")

    #Lessons
    print("[1] Lesson 1 (PRINT FUNCTION)")
    print("[2] Lesson 2 (VARIABLES)")
    print("[3] Lesson 3 (DATA TYPES)")
    print("[4] Lesson 4 (BASIC INPUT AND OUTPUT)")
    print("[5] Lesson 5 (CONDITIONAL STATEMENTS)")
    print("[6] Lesson 6 (NESTED CONDITION)")
    print("[7] Lesson 7 (LOGICAL OPERATOR)")
    print("[8] Lesson 8 (ITERATION AND LOOPS)")
    print("[9] Exit")

    print(f"\nWelcome To Python Tutorial System {name}!")

    #Choice
    lesson = input("\nEnter Lesson Number : ")

    #Lesson 1
    if lesson == "1":
        print(f"\nWelcome To Lesson 1 {name}!")
        print("In this lesson you are going to learn how to print using python language.")
        print("Our syntax in this lesson would be print("").")
        print("Where in we put a word inside the column for the computer to print.")

        print("\nprint - function that displays the output.")
        print("() - contains the information to be displayed.")
        print("value - text, number, or expression you want to show.")

        #Example
        print("\nFor Example :")
        print("Input : print(Hello World)")
        print("Output : Hello World")

        print("\nInput : print(9)")
        print("Output : 9")

        #Tip
        print("\nExtra tip to avoid confusion with your syntax, this python function is called comments.")
        print("There are mainly two types of comments.")

        print("\nFirst is hashtags [#] used for single line comments.")
        print("Second is triple duble quotes used for multi line comments")

        print("\nFor Example")
        print("#Student Info")
        print("Student Name :")
        print("Student Age :")
        print("Student Section :")

        print("\nThats all for lesson 1!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 2
    elif lesson == "2":
        print(f"\nWelcome To Lesson 2 {name}!")
        print("In this lesson you are going to learn how to use and know what variables are in python.")
        print("Our syntax for this lesson would be variable name = (its value).")
        print("A variables name could be anything as long as it doesnt start with numbers or special characters except underscore (_)")
        print("variables value can be a String or an Integer.")

        print("\nTake Note :")
        print("Variables are case sensitive. That means age and AGE are a whole different variable")

        #Example
        print("\nFor Example :")
        print("sample = 12 ")
        print("Input : print(sample)")
        print("Output : 12")

        #Tip
        print("\nExtra Tip : ")
        print("You can use print(f("")) when printing a variables value.")
        print("This python function is called f string.")

        print("\nFor Example :")
        print("Input :print(f value {sample})")
        print("Output : value 12")

        print("\nAnother Tip : ")
        print("You can also print multple variables at once using comma (,) .")

        print("\nFor Example :")
        print("a = I ")
        print("b = LOVE ")
        print("c = YOU ")
        print("Input : print(a, b, c)")
        print("Output : I LOVE YOU")

        print("\nCongratulations you just finished lesson 2!")
        print(f"Give it a shot {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 3
    elif lesson == "3":
        print(f"\nWelcome To Lesson 3 {name}!")
        print("In this lesson you are going to learn data types in python.")
        print("Python has four data types. We have String, Integer, Float, and Boolean.")

        print("\nString - text or characters inside quotes")
        print("Integer - whole numbers (no decimal)")
        print("Float - numbers with decimal point")
        print("Boolean - true or false")

        print("\nCongratulations you just finished lesson 3!")
        print(f"Give it a wild shot {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 4
    elif lesson == "4":
        print(f"\nWelcome To Lesson 4 {name}!")
        print("In this lesson you are going to learn the basic input and output function in python.")
        print("Our syntax for this lesson would be variable = input(prompt message)")
        print("All input is String type by default.")

        print("\nFor Example :")
        print("name = input(Enter Your Name :)")

        print("\nNext lets learn how to format the output!")
        print("name = input(Enter Your Name :)")
        print("print(Name :, name)")

        print("\nUsing that syntax would let you get the value of your input variable.")

        print("\nLastly lets learn how to convert input to other data types!")
        print("variable = (data type)input(prompt message))")
        print("For example lets turn it into an Integer.")
        print("variable = int(input(prompt message))")

        print("\nCongratulations you just finished lesson 4!")
        print(f"Give it a try {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 5
    elif lesson == "5":
        print(f"\nWelcome To Lesson 5 {name}!")
        print("In this lesson you are going to learn what conditional statements are and how to use them in python.")
        print("Conditional statements allows the program to make decisions based on whether the condition is True or False.")
        print("We have three conditional statements in python.")
        print("if, elif, and else.")

        #if condition
        print("\nFirst lets learn the if condition.")
        print("Structure :")
        print("if (condition) :")
        print("  statement")

        print("\nif - keyword that starts the conditional statement.")
        print("condition - if true, the idented statement is excecuted.")
        print("statement - the idented statement that runs when thr condition is true.")

        #Example (if)
        print("\nExample :")
        print("age = 18")
        print("if age >= 18 :")
        print("print(Legal Age)")

        print("\nIf age is 18 or more, the message (Legal Age) is printed.")
        print("If age is less than 18, nothing happens. ")

        #if-else condition
        print("\nNext lets learn the if-else condition.")

        print("\nStructure :")
        print("if (condition) :")
        print("  statement")
        print("else :")
        print("  statement")

        #Example (if-else)
        print("\nExample :")
        print("age = 18")
        print("if age >= 18 :")
        print("print(Legal Age)")
        print("else :")
        print("print(Minor)")

        print("\nIf age is 18 or more, the message (Legal Age) is printed.")
        print("If age is less than 18, the message (Minor) is printed. ")

        #if-elif-else condition
        print("\nMoving on lets learn the if-elif-else condition.")

        print("\nStructure :")
        print("if (condition) :")
        print("  statement")
        print("elif (condition) :")
        print("  statement")
        print("else :")
        print("  statement")

        #Example (if-elif-else)
        print("\nExample :")
        print("age = 18")
        print("if age == 18 :")
        print("print(Legal Age)")
        print("elif age > 18 :")
        print("print(Adult)")
        print("else :")
        print("print(Minor)")

        print("\nIf age is equal to 18, the message (Legal Age) is printed.")
        print("If age is greater than 18, the message (Adult) is printed. ")
        print("If both (if and elif) conditions are false, the message (Minor) is printed. ")

        #Additional Lesson
        print("\nadditionally in conditions we have relational operators. Also called as comparison operators.")

        print("="*30)
        print("COMPARISON OPERATORS")
        print("="*30)

        #Operators
        print("Equal to (==)")
        print("Example :")
        print("9 == 9 - True")
        print("10 == 9 - False")

        print("\nNot equal to (!=)")
        print("Example :")
        print("8 != 8 - False")
        print("8 != 9 - True")

        print("\nGreater than (>)")
        print("Example :")
        print("6 > 10 - False")
        print("11 > 3 - True")

        print("\nLess than (<)")
        print("Example :")
        print("4 < 10 - True")
        print("7 < 3 - False")

        print("\nGreater than or Equal to (>=)")
        print("Example :")
        print("15 >= 10 - True")
        print("12 >= 12 - True")
        print("4 >= 9 - False")
        print("20 >= 21 - False")

        print("\nLess than or Equal to (<=)")
        print("Example :")
        print("24 <= 26 - True")
        print("28 <= 28 - True")
        print("11 <= 7 - False")
        print("16 <= 13 - False")

        print("\nCongratulations you just finished lesson 5!")
        print(f"Give it a try {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 6
    elif lesson == "6":
        print(f"\nWelcome To Lesson 6 {name}!")
        print("In this lesson you are going to learn what nested condition is and how it works in python.")
        print("Nested conditions are simply a condition inside another condition.")

        print("\nStructure :")
        print("if (condition 1) :")
        print("   if (condition 2) :")
        print("  statement")
        print("   else :")
        print("  statement")
        print("else :")
        print("  statement")

        print("\nFor Example :")
        print("gender = input(Enter gender (M/F) : ")
        print("age = int(input(Enter age) : ")

        print("\nif gender == M :")
        print("   if age >= 21 :")
        print("  print(You are a Male Debutant.)")
        print("   else :")
        print("  print(Male but not debutant yet.)")
        print("else :")
        print("   if age >= 18 :")
        print("  print(You are a Female Debutant.)")
        print("   else :")
        print("  print(Female but not debutant yet.)")

        print("\nIf gender is equal to M and the age is more than or equal to 21, the message (You are a Male Debutant.) is printed.")
        print("If gender is equal to M and the age is less than to 21, the message (Male but not debutant yet.) is printed.")

        print("\nIf gender is equal to F and the age is more than or equal to 18, the message (You are a Female Debutant.) is printed.")
        print("If gender is equal to F and the age is less than to 18, the message (Female but not debutant yet.) is printed.")

        print("\nCongratulations you just finished lesson 6!")
        print(f"Give it a try {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 7
    elif lesson == "7":
        print(f"\nWelcome To Lesson 7 {name}!")
        print("In this lesson you are going to learn what logical operators are and how to use them in python.")
        print("Logical operators are used to combine or reverse conditions.")
        print("They are commonly used with if, elif, and else.")

        print("\nWe have three logical operators in python.")

        print("="*30)
        print("LOGICAL OPERATORS")
        print("="*30)

        #and
        print("and - both conditions must be true.")
        print("Example :")
        print("age = 20")
        print("has_if = True")

        print("\nif age >= 20 and has_id :")
        print("  print(You are allowed to enter.)")
        print("else :")
        print("  print(You are not allowed to enter.)")

        print("\nif both conditions (age) and (has_id) is true, the message (You are allowed to enter.) is printed")
        print("if both or one of the conditions (age) and (has_id) is false, the message (You are not allowed to enter.) is printed")

        #or
        print("\nor - at least one condition must be true.")
        print("Example :")
        print("day = saturday")

        print("\nif day == saturday or day == sunday :")
        print("  print(Its weekends!)")
        print("else :")
        print("  print(Its a regular day, keep it up!)")

        print("\nif one conditions (day) is true, the message (Its weekends!) is printed")
        print("if both of the conditions (day) is false, the message (Its a regular day, keep it up!) is printed")

        #not
        print("\nnot - reverses the result.")
        print("Example :")
        print("is_raining = False")

        print("\nif not is_raining :")
        print("  print(You can go outside.)")
        print("else :")
        print("  print(Bring an umbrella.)")

        print("\nThe variable (is_raining) is equal to False, so if (is_raining) not equal to (false) = is_raining is equal to (true). So the message (You can go outside.) is printed")
        print("If the variable (is_raining) is equal to True. If (is_raining) not equal to (true) = is_raining is equal to (false). So the message (Bring an umbrella.) is printed")

        print("\nCongratulations you just finished lesson 7!")
        print(f"Give it a try {name}!")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")

    #Lesson 8
    elif lesson == "8":
        print(f"\nWelcome To Lesson 8 {name}!")
        print("In this lesson you are going to learn iteration and loops and how to use them in python.")
        print("Iteration means repeating a process.")

        print("\n We have two types of loop.")
        print("We have for loop and while loop.")

        print("\nLets learn for loop first.")

        print("\nfor loop")
        print("Repeats instructions for each item in a sequence. ")

        print("\nSyntax :")
        print("for (variable) in (sequence) :")
        print("  (statement) ")

        print("\nvariable - receives each item. ")
        print("sequence - items to loop through. ")
        print("statement - the loop body")

        print("\nFor Example :")
        print("Input :")
        print("for number in range(4) :")
        print("  print(Study Python) ")

        print("Output :")
        for number in range(4):
            print("Study Python")

        print("\nNext what if we want the system to count from 1 to 5?")

        print("\nInput :")
        print("for number in range(1, 6) :")
        print("  print(number) ")

        print("Output :")
        for number in range(1, 6):
            print(number)

        print("\nHow it works :")
        print("Start value 1 is included, the stop value 6 is excluded. ")
        print("Each iteration assigns the next value to our variable (number) ")
        print("print(number) displays that value, after 5 loop ends. ")

        print("\nNow what if we want the system to count down from 5 to 1?")

        print("\nInput :")
        print("for number in range(5, 0, -1) :")
        print("  print(number)")

        print("Output :")
        for number in range(5, 0, -1):
            print(number)

        print("\nHow it works :")
        print("Value starts at 5. ")
        print("Stops before 0.")
        print("-1 decreases value by 1. ")
        print("print(number) prints the value of variable (number). ")

        print("\nLastly let's learn while loop. ")

        print("\nwhile loop")
        print("Repeats instructions when a condition is true. ")

        print("\nSyntax :")
        print("while (condition) :")
        print("  (statement) ")

        print("\ncondition - checked before each iteration. ")
        print("statement - runs while the condition is true. ")

        print("\nFor Example :")
        print("Input :")
        print("count = 1")
        print("while count <= 5 :")
        print("  print(count) ")
        print("  count += 1")

        print("Output :")
        count = 1
        while count <= 5:
            print(count)
            count += 1

        print("\nNow what if we want the system to count down from 5 to 1?")

        print("\nInput :")
        print("count = 5")
        print("while count >= 1 :")
        print("  print(count) ")
        print("  count -= 1")

        print("Output :")
        count = 5
        while count >= 1:
            print(count)
            count -= 1

        print("\nHow it works :")
        print("Value starts at 5. ")
        print("Repeats while count is greater than or equal to 1.")
        print("count -=1 decreases value by 1. ")
        print("print(number) prints the value of variable (number). ")
        print("Stops when the condition is false (when count is less than 1).")

        print(f"\nThats all for lesson 8 {name}, give iterations and loops a try! ")

        while True:
            print("\n[1] Learn Another Lesson")
            print("[2] Exit")

            user = input("\nWould you like to learn another lesson? Choose 1 or 2: ")

            if user == "1":
                break

            elif user == "2":
                print(f"\nThank you for using this system {name}!")
                exit()

            else:
                print("\nInvalid input! Please choose 1 or 2.")
                
    elif lesson == "9" :
        print("\nSystem shutting down...")
        break
    
    else :
        print("\nInvalid Input Try Again. ")

#Quiz Data
quizzes = {
    "1": [
        ("What is the purpose of print()?",
         ["To receive input", "To display output", "To create variables", "To delete information"], "B"),
        ("Which is the correct syntax for printing Hello World?",
         ["print(Hello World)", "print = Hello World", 'print("Hello World")', "output(Hello World)"], "C"),
        ("What do parentheses () contain in print()?",
         ["Information to display", "Variable names only", "Comments", "Loops"], "A"),
        ("Which symbol is used for a single-line comment?",
         ["//", "#", "&&", "**"], "B"),
        ("What is the output of print(9)?",
         ["Nine", "Error", "9", "print(9)"], "C")
    ],

    "2": [
        ("What is a variable?",
         ["A storage for data", "A print function", "A loop", "A comment"], "A"),
        ("Which is a valid variable name?",
         ["2name", "my-name", "_name", "@name"], "C"),
        ("Are Python variable names case-sensitive?",
         ["No", "Yes", "Sometimes", "Only numbers"], "B"),
        ("What is the output of sample = 12 followed by print(sample)?",
         ["sample", "12", "Error", "None"], "B"),
        ("What is used to print variables inside a formatted string?",
         ["F-string", "While loop", "If statement", "Input loop"], "A")
    ],

    "3": [
        ("Which data type is used for text?",
         ["Integer", "Float", "String", "Boolean"], "C"),
        ("Which data type represents whole numbers?",
         ["String", "Integer", "Float", "Boolean"], "B"),
        ("What data type is 3.14?",
         ["Integer", "String", "Boolean", "Float"], "D"),
        ("What are the two Boolean values?",
         ["Yes and No", "1 and 2", "True and False", "On and Off"], "C"),
        ("What is the data type of 'Python'?",
         ["String", "Integer", "Float", "Boolean"], "A")
    ],

    "4": [
        ("Which function is used to receive user input?",
         ["print()", "input()", "int()", "range()"], "B"),
        ("What is the default data type of input()?",
         ["Integer", "Float", "String", "Boolean"], "C"),
        ("Which function converts input into an integer?",
         ["str()", "float()", "bool()", "int()"], "D"),
        ("What does print() do?",
         ["Displays output", "Receives input", "Converts strings", "Creates loops"], "A"),
        ("Which is the correct way to receive an integer input?",
         ["input(int())", "int(input('Enter age: '))", "print(input())", "integer(input())"], "B")
    ],

    "5": [
        ("What are the three conditional keywords in Python?",
         ["for, while, break", "print, input, int", "if, elif, else", "and, or, not"], "C"),
        ("What happens if an if condition is True?",
         ["The statement executes", "The program closes", "The condition is deleted", "Nothing happens"], "A"),
        ("Which operator means equal to?",
         ["=", "==", "!=", ">="], "B"),
        ("What does the else statement do?",
         ["Repeats a condition", "Creates a variable", "Runs when previous conditions are false", "Displays input"], "C"),
        ("What is the result of 10 > 5?",
         ["False", "10", "5", "True"], "D")
    ],

    "6": [
        ("What is a nested condition?",
         ["A loop inside a loop", "A condition inside another condition", "A variable inside a string", "A function inside print()"], "B"),
        ("Which keyword starts a conditional statement?",
         ["if", "for", "print", "input"], "A"),
        ("What determines whether an inner condition executes?",
         ["The variable name", "The print function", "The outer condition", "The comment"], "C"),
        ("What happens if the outer condition is False?",
         ["The inner condition automatically runs", "The outer else block can execute", "The program always crashes", "All variables are deleted"], "B"),
        ("Which statement can be placed inside another if statement?",
         ["Another if statement", "Only print()", "Only input()", "None of the above"], "A")
    ],

    "7": [
        ("How many logical operators are there in Python?",
         ["Two", "Four", "Three", "Five"], "C"),
        ("What does the AND operator require?",
         ["Both conditions must be True", "Only one condition must be True", "Both conditions must be False", "No conditions are needed"], "A"),
        ("What does the OR operator require?",
         ["Both conditions must be False", "At least one condition must be True", "Both conditions must be True", "No conditions are needed"], "B"),
        ("What does the NOT operator do?",
         ["Combines two variables", "Adds two numbers", "Repeats a condition", "Reverses a Boolean value"], "D"),
        ("What is the result of True and False?",
         ["True", "False", "None", "Error"], "B")
    ],

    "8": [
        ("What does iteration mean?",
         ["Repeating a process", "Deleting a variable", "Receiving input", "Creating a comment"], "A"),
        ("What are the two main types of loops in Python?",
         ["if and else", "and and or", "for and while", "print and input"], "C"),
        ("What does range(1, 6) produce?",
         ["1, 2, 3, 4, 5, 6", "1, 2, 3, 4, 5", "0, 1, 2, 3, 4, 5", "2, 3, 4, 5, 6"], "B"),
        ("When does a while loop stop?",
         ["When the condition becomes False", "When the condition is True", "After one iteration always", "When print() executes"], "A"),
        ("What does count += 1 do?",
         ["Subtracts 1 from count", "Multiplies count by 1", "Adds 1 to count", "Deletes count"], "C")
    ]
}


#Quiz Function
def run_quiz(name, lesson_number):
    questions = quizzes[lesson_number]
    score = 0

    print("\n" + "=" * 30)
    print(f"LESSON {lesson_number} QUIZ")
    print("=" * 30)
    print("There are 5 questions.")
    print("Choose A, B, C, or D.")

    for number, (question, choices, correct_answer) in enumerate(questions, start=1):
        print("\n" + "-" * 30)
        print(f"Question {number}: {question}")
        print("-" * 30)

        for letter, choice in zip(["A", "B", "C", "D"], choices):
            print(f"[{letter}] {choice}")

        while True:
            answer = input("\nYour answer: ").strip().upper()

            if answer in ["A", "B", "C", "D"]:
                break
            else:
                print("Invalid input! Choose A, B, C, or D.")

        if answer == correct_answer:
            print("Correct! Good job!")
            score += 1
        else:
            print(f"Wrong! The correct answer is {correct_answer}.")

    percentage = (score / 5) * 100

    print("\n" + "=" * 30)
    print("QUIZ RESULTS")
    print("=" * 30)
    print(f"Student Name: {name}")
    print(f"Lesson: {lesson_number}")
    print(f"Your Score: {score}/5")
    print(f"Percentage: {percentage:.0f}%")

    if score == 5:
        print("Excellent! Perfect score!")
    elif score >= 3:
        print("Good job! Keep practicing!")
    else:
        print("Keep studying! You can do better next time!")

    print("=" * 30)


#Intro
name = input("Enter Student Name: ")
print(f"Welcome To Python Tutorial System {name}!")
print("=" * 30)


#Menu
while True:

    print("\n" + "=" * 30)
    print("PYTHON TUTORIAL SYSTEM")
    print("=" * 30)

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

    lesson = input("\nEnter Lesson Number: ")

    #Lesson 1
    if lesson == "1":

        print(f"\nWelcome To Lesson 1 {name}!")
        print("In this lesson you are going to learn how to print using python language.")
        print('Our syntax in this lesson would be print("").')
        print("Wherein we put a word inside the column for the computer to print.")

        print("\nprint - function that displays the output.")
        print("() - contains the information to be displayed.")
        print("value - text, number, or expression you want to show.")

        print("\nFor Example:")
        print('Input: print("Hello World")')
        print("Output: Hello World")

        print("\nInput: print(9)")
        print("Output: 9")

        print("\nExtra tip: Comments are used to explain code.")
        print("There are mainly two types of comments.")

        print("\nFirst is hashtags [#] used for single-line comments.")
        print("Second is triple quotes used for multi-line strings.")

        print("\nFor Example:")
        print("#Student Info")
        print("Student Name:")
        print("Student Age:")
        print("Student Section:")

        print("\nThats all for lesson 1!")

        run_quiz(name, "1")

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
        print("Our syntax for this lesson would be variable_name = value.")
        print("A variable name could be anything as long as it doesnt start with numbers or special characters except underscore (_).")
        print("Variable values can be a String, Integer, Float, or other data types.")

        print("\nTake Note:")
        print("Variables are case sensitive. That means age and AGE are different variables.")

        print("\nFor Example:")
        print("sample = 12")
        print("Input: print(sample)")
        print("Output: 12")

        print("\nExtra Tip:")
        print('You can use print(f"value {sample}") when printing a variable value.')
        print("This is called an f-string.")

        print("\nFor Example:")
        print('Input: print(f"value {sample}")')
        print("Output: value 12")

        print("\nAnother Tip:")
        print("You can also print multiple variables at once using comma (,).")

        print("\nFor Example:")
        print('a = "I"')
        print('b = "LOVE"')
        print('c = "YOU"')
        print("Input: print(a, b, c)")
        print("Output: I LOVE YOU")

        print("\nCongratulations you just finished lesson 2!")
        print(f"Give it a shot {name}!")

        run_quiz(name, "2")
        
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
        print("Python has four basic data types: String, Integer, Float, and Boolean.")

        print("\nString - text or characters inside quotes")
        print("Integer - whole numbers (no decimal)")
        print("Float - numbers with decimal point")
        print("Boolean - True or False")

        print("\nCongratulations you just finished lesson 3!")
        print(f"Give it a wild shot {name}!")

        run_quiz(name, "3")
        
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
        print("Our syntax for this lesson would be variable = input(prompt message).")
        print("All input is String type by default.")

        print("\nFor Example:")
        print('name = input("Enter Your Name: ")')

        print("\nNext lets learn how to format the output!")
        print('name = input("Enter Your Name: ")')
        print('print("Name:", name)')

        print("\nUsing that syntax would let you get the value of your input variable.")

        print("\nLastly lets learn how to convert input to other data types!")
        print("variable = int(input(prompt message))")
        print("For example lets turn it into an Integer.")

        print("\nCongratulations you just finished lesson 4!")
        print(f"Give it a try {name}!")

        run_quiz(name, "4")

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
        print("Conditional statements allow the program to make decisions based on whether the condition is True or False.")
        print("We have three conditional statements in Python.")
        print("if, elif, and else.")

        print("\nFirst lets learn the if condition.")
        print("Structure:")
        print("if condition:")
        print("    statement")

        print("\nif - keyword that starts the conditional statement.")
        print("condition - if true, the indented statement is executed.")
        print("statement - the indented statement that runs when the condition is true.")

        print("\nExample:")
        print("age = 18")
        print("if age >= 18:")
        print('    print("Legal Age")')

        print("\nIf age is 18 or more, the message Legal Age is printed.")
        print("If age is less than 18, nothing happens.")

        print("\nNext lets learn the if-else condition.")

        print("\nStructure:")
        print("if condition:")
        print("    statement")
        print("else:")
        print("    statement")

        print("\nExample:")
        print("age = 18")
        print("if age >= 18:")
        print('    print("Legal Age")')
        print("else:")
        print('    print("Minor")')

        print("\nIf age is 18 or more, Legal Age is printed.")
        print("If age is less than 18, Minor is printed.")

        print("\nMoving on lets learn the if-elif-else condition.")

        print("\nStructure:")
        print("if condition:")
        print("    statement")
        print("elif condition:")
        print("    statement")
        print("else:")
        print("    statement")

        print("\nExample:")
        print("age = 18")
        print("if age == 18:")
        print('    print("Legal Age")')
        print("elif age > 18:")
        print('    print("Adult")')
        print("else:")
        print('    print("Minor")')

        print("\nIf age is equal to 18, Legal Age is printed.")
        print("If age is greater than 18, Adult is printed.")
        print("If both conditions are false, Minor is printed.")

        print("\nAdditionally in conditions we have relational operators.")

        print("=" * 30)
        print("COMPARISON OPERATORS")
        print("=" * 30)

        print("\nEqual to (==)")
        print("9 == 9 - True")
        print("10 == 9 - False")

        print("\nNot equal to (!=)")
        print("8 != 8 - False")
        print("8 != 9 - True")

        print("\nGreater than (>)")
        print("6 > 10 - False")
        print("11 > 3 - True")

        print("\nLess than (<)")
        print("4 < 10 - True")
        print("7 < 3 - False")

        print("\nGreater than or Equal to (>=)")
        print("15 >= 10 - True")
        print("12 >= 12 - True")
        print("4 >= 9 - False")
        print("20 >= 21 - False")

        print("\nLess than or Equal to (<=)")
        print("24 <= 26 - True")
        print("28 <= 28 - True")
        print("11 <= 7 - False")
        print("16 <= 13 - False")

        print("\nCongratulations you just finished lesson 5!")
        print(f"Give it a try {name}!")

        run_quiz(name, "5")

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

        print("\nStructure:")
        print("if condition 1:")
        print("    if condition 2:")
        print("        statement")
        print("    else:")
        print("        statement")
        print("else:")
        print("    statement")

        print("\nFor Example:")
        print('gender = input("Enter gender (M/F): ")')
        print('age = int(input("Enter age: "))')

        print("\nif gender == 'M':")
        print("    if age >= 21:")
        print('        print("You are a Male Debutant.")')
        print("    else:")
        print('        print("Male but not debutant yet.")')
        print("else:")
        print("    if age >= 18:")
        print('        print("You are a Female Debutant.")')
        print("    else:")
        print('        print("Female but not debutant yet.")')

        print("\nIf gender is M and age is at least 21, the male debutant message is printed.")
        print("If gender is M and age is less than 21, the male not-yet-debutant message is printed.")

        print("\nIf gender is F and age is at least 18, the female debutant message is printed.")
        print("If gender is F and age is less than 18, the female not-yet-debutant message is printed.")

        print("\nCongratulations you just finished lesson 6!")
        print(f"Give it a try {name}!")

        run_quiz(name, "6")

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

        print("\nWe have three logical operators in Python.")

        print("=" * 30)
        print("LOGICAL OPERATORS")
        print("=" * 30)

        print("\nand - both conditions must be true.")
        print("Example:")
        print("age = 20")
        print("has_id = True")

        print("\nif age >= 20 and has_id:")
        print('    print("You are allowed to enter.")')
        print("else:")
        print('    print("You are not allowed to enter.")')

        print("\nBoth conditions must be true for entry to be allowed.")

        print("\nor - at least one condition must be true.")
        print("Example:")
        print("day = 'saturday'")

        print("\nif day == 'saturday' or day == 'sunday':")
        print('    print("Its weekends!")')
        print("else:")
        print('    print("Its a regular day, keep it up!")')

        print("\nAt least one condition must be true for the weekend message to appear.")

        print("\nnot - reverses the result.")
        print("Example:")
        print("is_raining = False")

        print("\nif not is_raining:")
        print('    print("You can go outside.")')
        print("else:")
        print('    print("Bring an umbrella.")')

        print("\nThe NOT operator reverses the Boolean value.")
        print("If is_raining is False, not is_raining becomes True.")

        print("\nCongratulations you just finished lesson 7!")
        print(f"Give it a try {name}!")

        run_quiz(name, "7")

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

        print("\nWe have two types of loops.")
        print("We have for loop and while loop.")

        print("\nLets learn for loop first.")

        print("\nfor loop")
        print("Repeats instructions for each item in a sequence.")

        print("\nSyntax:")
        print("for variable in sequence:")
        print("    statement")

        print("\nvariable - receives each item.")
        print("sequence - items to loop through.")
        print("statement - the loop body.")

        print("\nFor Example:")
        print("Input:")
        print("for number in range(4):")
        print('    print("Study Python")')

        print("Output:")
        for number in range(4):
            print("Study Python")

        print("\nNext what if we want the system to count from 1 to 5?")

        print("\nInput:")
        print("for number in range(1, 6):")
        print("    print(number)")

        print("Output:")
        for number in range(1, 6):
            print(number)

        print("\nHow it works:")
        print("Start value 1 is included, the stop value 6 is excluded.")
        print("Each iteration assigns the next value to number.")

        print("\nNow what if we want the system to count down from 5 to 1?")

        print("\nInput:")
        print("for number in range(5, 0, -1):")
        print("    print(number)")

        print("Output:")
        for number in range(5, 0, -1):
            print(number)

        print("\nHow it works:")
        print("Value starts at 5.")
        print("Stops before 0.")
        print("-1 decreases value by 1.")

        print("\nLastly let's learn while loop.")

        print("\nwhile loop")
        print("Repeats instructions when a condition is true.")

        print("\nSyntax:")
        print("while condition:")
        print("    statement")

        print("\ncondition - checked before each iteration.")
        print("statement - runs while the condition is true.")

        print("\nFor Example:")
        print("Input:")
        print("count = 1")
        print("while count <= 5:")
        print("    print(count)")
        print("    count += 1")

        print("Output:")
        count = 1
        while count <= 5:
            print(count)
            count += 1

        print("\nNow what if we want the system to count down from 5 to 1?")

        print("\nInput:")
        print("count = 5")
        print("while count >= 1:")
        print("    print(count)")
        print("    count -= 1")

        print("Output:")
        count = 5
        while count >= 1:
            print(count)
            count -= 1

        print("\nHow it works:")
        print("Value starts at 5.")
        print("Repeats while count is greater than or equal to 1.")
        print("count -= 1 decreases value by 1.")
        print("Stops when the condition is false.")

        print(f"\nThats all for lesson 8 {name}, give iterations and loops a try!")

        run_quiz(name, "8")
        
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

    #Exit
    elif lesson == "9":
        print("\nSystem shutting down...")
        print(f"Thank you for using this system {name}!")
        break

    
    else:
        print("\nInvalid Input! Try Again.")

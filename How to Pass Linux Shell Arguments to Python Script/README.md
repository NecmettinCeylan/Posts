# How to Pass Linux Shell Arguments to Python Script
## Simple steps to use linux shell arguments in your python scripts 

# Get passed variables using sys module

All you need to do is get passed variables using sys.argv and set them to a variable
then you this variable.

    import sys
    variable_1 = sys.argv[1]
    variable_2 = sys.argv[2]


# When passed less than expected shell arguments raises IndexError

    import sys

    # 0 index argument is filename
    # as you can see from this print
    print(sys.argv)

    # we expect to get exactly two 
    # arguments for this script
    # not to forget with file name list length is 3
    if len(sys.argv) < 3:
        raise Exception("Please pass two arguments")
        
    if len(sys.argv) > 3:
        raise Exception("Too many arguments passed")

    variable_1 = sys.argv[1]
    variable_2 = sys.argv[2]

    print("First arg: ", variable_1)
    print("Second arg: ", variable_2)
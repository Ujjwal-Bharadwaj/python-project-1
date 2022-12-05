# python-project-1


'''
Python Project to Find if it is possible to cut the cake in below-mentioned ways for a given value of N.
Given an integer N and a cake which can be cut into pieces, each cut should be a straight line going from the center
of the cake to its border. Also, the angle between any two cuts must be a positive integer. Two pieces are equal
if their appropriate angles are equal.
The given cake can be cut in following three ways:
1. Cut the cake into N equal pieces.
2. Cut the cake into N pieces of any size.
3. Cut the cake into N pieces such that no two of them are equal.
'''

print("WELCOME")

def cake():
    input1 = int(input("How many parts you want to cut the cake in:\n"))
    print('1. Check if cake can be cut into n pieces of equal size')
    print('2. Check if cake can be cut into n pieces of any size')
    print('3. Check if cake can be cut into n pieces such that no two of them are of equal size')
    ch = int(input('Enter your choice(1,2,3): '))
    if ch == 1:
        if 360 % input1 == 0:
            print()
            print(f"Yes, the cake can be cut into {input1} different pieces of equal size")
            a = 360 / input1
            b = chr(176)
            print(f'The angle of one piece of cake will be of: {a}{b}')
            print()
        else:
            print()
            print(f"No, the cake cannot be cut into {input1} different pieces of equal size")
            print()
    elif ch == 2:
        if input1 < 360:
            print()
            print(f"Yes, the cake can cut into {input1} pieces of any size")
            print()
        else:
            print()
            print(f"No, the cake cannot cut into {input1} pieces of any size")
            print()
    elif ch == 3:
        if input1 * (input1 + 1) / 2 <= 360:
            print()
            print(f"Yes, the cake can cut into {input1} pieces such that no two of them are equal")
            print()
        else:
            print()
            print(f"No, the cake can cut into {input1} pieces such that no two of them are equal")
            print()
    else:
        print()
        print('Enter a valid choice')
        print()


switch = True
while switch:
    cake()
    again = input("Type 'yes' if you want to run the program again type 'no' for exit:\n")
    if again == 'no' or again == 'NO' or again == 'No':
        switch = False
    print("Thank you")

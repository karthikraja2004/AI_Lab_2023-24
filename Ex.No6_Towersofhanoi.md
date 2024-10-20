# Ex.No: 6   Logic Programming – Tower Of Hanoi
### DATE: 23-09-2024
### NAME: NANDA KISHORE R
### REGISTER NUMBER : 212222060157 
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
3.  a )	If only one disk  => Move disk from X to Y.
4.  b)	If Number of disk greater than 0 then
5.        i)	Move  N-1 disks from X to Z.
6.        ii)	Move  Nth disk from X to Y
7.        iii)	Move  N-1 disks from Y to X.
8. Run the program  to find answer of  query.

### Program:
```
def tower_of_hanoi(n, source, target, auxiliary):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}.")
        return
    # Step 1: Move n-1 disks from source to auxiliary
    tower_of_hanoi(n - 1, source, auxiliary, target)
    
    # Step 2: Move the nth disk from source to target
    print(f"Move disk {n} from {source} to {target}.")
    
    # Step 3: Move n-1 disks from auxiliary to target
    tower_of_hanoi(n - 1, auxiliary, target, source)

# Sample input
number_of_disks = 3  # Change this value to test with a different number of disks
tower_of_hanoi(number_of_disks, 'A', 'C', 'B')
```

### Output:

<img src = "https://github.com/user-attachments/assets/7e6c3482-a18e-4933-a23a-d01f2b13ec75" width="600">

### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.

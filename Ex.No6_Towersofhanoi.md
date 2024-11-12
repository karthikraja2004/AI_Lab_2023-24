# Ex.No: 6   Logic Programming – Tower Of Hanoi
### DATE: 09-09-2024
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
% Base case: If there's only one disk, move it from Source to Destination.
move(1, Source, Destination, _) :- 
    write('Move disk from '), 
    write(Source), 
    write(' to '), 
    write(Destination), 
    nl.

% Recursive case: Move N disks from Source to Destination using Helper.
move(N, Source, Destination, Helper) :-
    N > 1,
    N1 is N - 1,
    move(N1, Source, Helper, Destination),  % Move N-1 disks from Source to Helper
    move(1, Source, Destination, _),        % Move the Nth disk from Source to Destination
    move(N1, Helper, Destination, Source).  % Move N-1 disks from Helper to Destination

```

### Output:

<img src = "https://github.com/user-attachments/assets/3b84d4a5-9951-47cf-a39d-4f1e739d176a" width="600">

### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.

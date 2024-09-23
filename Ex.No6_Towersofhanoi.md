# Ex.No: 6   Logic Programming – Towers of Hanoi
### DATE:                                                                            
### REGISTER NUMBER : 
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
% Base case: If there is only one disk, move it from Source to Destination.
move(1, Source, Destination, _) :-
    format('Move disk 1 from ~w to ~w.~n', [Source, Destination]).

% Recursive case: Move N-1 disks from Source to Auxiliary, then move the Nth disk to Destination, and finally move N-1 disks from Auxiliary to Destination.
move(N, Source, Destination, Auxiliary) :-
    N > 1,
    M is N - 1,
    move(M, Source, Auxiliary, Destination), % Move N-1 disks from Source to Auxiliary
    format('Move disk ~w from ~w to ~w.~n', [N, Source, Destination]), % Move the Nth disk from Source to Destination
    move(M, Auxiliary, Destination, Source). % Move
```



### Output:
![towers of hanoi](https://github.com/user-attachments/assets/8cbf0b36-1978-4f0a-a35a-13e2a0e37aed)




### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.

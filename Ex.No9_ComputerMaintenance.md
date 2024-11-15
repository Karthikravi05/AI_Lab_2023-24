# Ex.No: 9  Logic Programming –  Computer Maintenance Expert System
### DATE:  07/10/2024                                                                          
### REGISTER NUMBER : 212221060117
### AIM: 
Write a Prolog program to build a computer maintenance expert system.
###  Algorithm:
1. Start the program.
2. Write the rules for each fault in computer.
3. If system have printing problem, missing dots and no uniform printing then system fault on printer head.
4. If system have not printing, missing dots and spread inks then system fault on ribbon
5. If system have not printing, paper jam and out of paper then system fault on paper stuck in printer
6. Similarly define rules for all faults.
7. Define facts for system problems.
8. Find the fault of computer by passing query to system.
     
### Program:

```
fault(printer_head) :-
	problem(not_printing),
	problem(missing_dots),
	problem(nonuniform_printing).
fault(ribbon) :-
	problem(not_printing),
	problem(missing_dots),
	problem(spread_ink).
fault(paper) :-
	problem(not_printing),
	problem(paper_jam),
	problem(out_of_paper).
fault(motherboard) :-
	problem(long_beep),
	problem(short_beep).
fault(hard_disc) :-
	problem(two_short_beeps),
	problem(blank_display).
problem(not_printing).
problem(missing_dots).
problem(spread_ink).
problem(two_short_beeps).
problem(blank_display).
```


### Output:

![Screenshot 2024-10-07 095244](https://github.com/user-attachments/assets/432cfedf-fc99-4fa4-befd-bf84a623fc17)

![Screenshot 2024-10-07 095314](https://github.com/user-attachments/assets/55a7fece-8f8e-47ed-95af-d10dd324ff19)

![Screenshot 2024-10-07 095333](https://github.com/user-attachments/assets/7158859a-3a62-4b9b-b853-c5feb1a82bb3)

![Screenshot 2024-10-07 095357](https://github.com/user-attachments/assets/ce0ef70b-6ef4-4d9a-a59c-49d89a85c0c0)

![Screenshot 2024-10-07 095416](https://github.com/user-attachments/assets/ec2fd22b-d301-4627-89ee-aca5078a01e9)

### Result:
Thus the simple omputer maintenance expert system was built sucessfully.

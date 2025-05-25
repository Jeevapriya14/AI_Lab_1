# Ex.No: 9  Logic Programming –  Computer Maintenance Expert System
                                                                          
### REGISTER NUMBER : 212222220006
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
![369883868-ed5bfa3f-c982-4e48-a974-4f627987fe3c](https://github.com/user-attachments/assets/3065905b-53de-421c-bb32-7f8874498fbf)




### Result:
Thus the simple omputer maintenance expert system was built sucessfully.

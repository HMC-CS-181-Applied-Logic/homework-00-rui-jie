## Part a

### Describe what the code in `z3-test.py` is doing in a paragraph or two.

We are first given four variables, two booleans a and b, as well as two integers x and y. f is a boolean formula which is a conjunction of five formulas: Not(a), b, x > 0, x < 100, x < y. solver is a Solver object. solver.add(f) adds boolean formula f to solver. Then, f_check (solver.check()) checks if there is an assignment of the given variables such that all of the formulas are satisfied. Afterwards, the if statement, if (f_check == sat):, checks if the solver figured out an assignment of variables such that all of its formulas are true. If so, print(solver.model()) prints one such assignment. In this case, where there is only formula f in solver, if_check does equal sat since f can be satisfied with the assignment a = False, b = True, x = 99 y = 100. Thus, the solver.model() is printed, which is an assignment of the variables such that all the formulas are satisfied. 

After this, the formula y < 1 is added to solver, and solver.check() is called again. This time, there is no assignment of the four variables a,b,x, and y such that both formula f and y < 1 are fulfilled. Thus, "unsat" is printed, and, since the conditional is not fulfilled, solver.model() is not printed. 

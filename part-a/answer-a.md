## Part a

We are first given four variables, two booleans a and b, as well as two integers x and y. f is a a conjunction of five formulas: Not(a), b, x > 0, x < 100, x < y. solver is a Solver object. solver.add(f) adds boolean formula f to solver. Then, f_check (solver.check()) checks if there is an interpretation that satisfies each of the logical formulas. If there is such an interpretation, print(solver.model()) prints it. In this case, where there is only formula f in solver, if_check does equal sat since f can be satisfied with  a = False, b = True, x = 99 y = 100. Thus, solver.model() is printed.

After this, the formula y < 1 is added to solver, and solver.check() is called again. This time, there is no interpretation that satisfies formula f and y < 1. Thus, "unsat" is printed, and, since there is no interpretation that satisfies each of the logical formulas, solver.model() is not printed.

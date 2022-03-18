# Very Large Scale Integration problem - CDMO project Module I

This is the repository for the project of Combinatorial and Decision Making Optimization Module I of University of Bologna.

The aim of the project is to try different approaches to solve the optimization problem of very large scale integration. The approaches tried 
include Constraint Programming (CP), propositional SATisfiability (SAT) and/or its extension to Satisfiability Modulo Theories (SMT).

The problem can be formulated as: given a fixed-width plate and a list of rectangular circuits, decide how to place them
on the plate so that the length of the final device is minimized. 

An exhaustive description of the work done can be read in the report. For SMT and SAT formulations i used notebooks since the library Z3Py has some problems
at being imported in a PyCharm environment, while for CP encodings i wrote a script in python which uses the library _minizinc_ and can be run from command 
line from the working directory as `solver.py` with the following commands:

  - `-i`, `--instances` : followed by `all` or a list of integers e.g. `1,21,33` to indicate the instances to be solved - default = `all`
  - `-o`, `--output` : followed by the name of the output directory where results will be written - default = `out`
  - `-t`, `--timeout` : followed by the timeout value for solving instances in seconds - default = `300` (5mins)
  - `-r`, `--rotation` : a boolean variable to indicate whether rotation is allowed or not - default = `False`
  - `-p`, `--plot` : a boolean variable to indicate whether to plot grids for the solutions and save them - default = `False`

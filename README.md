# Tcl Number Comparison Bug

This repository demonstrates a common error in Tcl related to number comparison using the `==` operator.  The `==` operator performs string comparison, not numerical comparison, which can lead to unexpected behavior if not handled carefully. 

The `bug.tcl` file contains code illustrating the problem. The `bugSolution.tcl` file provides a corrected version using the `expr` command for numerical comparison.

## Bug Description
The `badproc` procedure is designed to compare two numbers and return 1 if they are equal, and 0 otherwise. However, because it uses the `==` operator directly, it does string comparison. This may produce unintended results, for example, comparing "10" and "100" will return true.
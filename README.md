# Unexpected Results with Negative Input in Julia Function

This repository demonstrates a common error in Julia functions when handling negative inputs. The `myfunction` function intends to return the square of the input, regardless of its sign. However, due to the way negative numbers are handled in the `else` statement, the function produces unexpected results.

## Bug
The bug lies in the `else` statement, where `-x^2` is used. This means the square of x is calculated and then negated, which is not the intended behavior. 

## Solution
The solution involves simply returning `x^2` in the `else` statement as well, effectively ensuring the function always returns the square regardless of the input's sign.

## How to reproduce
1. Clone this repository
2. Open a Julia REPL or script
3. Run the `bug.jl` file to see the unexpected results
4. Run the `bugSolution.jl` file to see the correct results
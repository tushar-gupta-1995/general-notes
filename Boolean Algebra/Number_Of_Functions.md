Given we have n boolean variables, then there are 2^n possible combinations of these variables.
Each combination out of 2^n combinations can be treated as an input to a function.
Now question is how many such functions are possible?
Now while each combination out of 2^n represents input to function, the output can only be 2 i.e 1 or 0 due to boolean nature.

Thus for each input we have 2 functions, one outputting 1 and other 0, and we have 2^n inputs so total functions are 2^(2^n).
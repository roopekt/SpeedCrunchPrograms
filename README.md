# SpeedCrunchPrograms
SpeedCrunch is a scientfic calculator. It has just enough features to make some form of programming possible, even though it isn't even Turing complete. This repository contains some programs that run inside the calculator.

## SpeedCrunch features

The two things that allow programming are functions (arbitary number of inputs, single number as output) and the `ans` variable. The `ans` variable contains the result of the last evaluated expression, and it's contents are printed after each evaluation. `ans` can thus be used as storage and output. SpeedCrunch has custom variables too, but they must be assigned to by the user which makes them unusable as anything but constants. SpeedCrucnh doesn't support recursion, loops, conditionals or random numbers. All data is floating point (about 50 decimal digits, and another 50 if complex numbers are used). "Programs" can be exported and imported as json.

## Work arounds for basic programming constructs

- booleans

  0 and 1
- conditionals

  all possibilities must be evaluated: `f(x; flag) = (1-flag)*a(x) + flag*b(x)`
- loops
  
  Manual recursion can be used for a fixed number of iterations. Iteration index can be passed as a parameter:\
  `loop_3_times(x) = f(f(f(x;0);1);2)`
  
- random numbers
  
  `ans` can be hashed:\
  `hashf_iter(x) = abs(frac(sin(943x+732)*298))`\
  `random01() = hashf_iter(hashf_iter(hashf_iter(real(ans)+imag(ans))))`
  
- comparison

  `sign(x)` function (-1 if negative, 0 if 0, 1 if positive) is the easiest to use for comparison:\
  `equals(a; b) = 1-abs(sign(a-b))` (rounding errors shouldn't break this if only integers are used)
  
## Usage

 1. Open the json file through `Session/Open`
 2. Follow the instructions for the specific program
    

# console-pong
This is a pong game I made following this YouTube tutorial by NVitanovic: https://www.youtube.com/watch?v=y8QL62SDlcQ

I made this as a refresher to C++ after not coding for some 3 months in the language.
Most of the concepts I understood, but I was able to learn new things:
  - "friend" : 
               -Allows functions to call private variables in a class without writing get() functions.
               -Commonly used in overloading stream operators (see lines 64 and 93 which were used for debugging).
               
  - "inline" : 
               -Allows faster execution of a function by saving overhead time.
               -Instead of holding a memory address to find the function's definition to execute, the compiler executes the function on the spot.
               -Functions can also be defined in a "header .h" file with this keyword.
               -Modern compilers will automatically make functions "inline" if needed without the use of the keyword.
               
  - "conditional operator" :
               -Allows an if-else-statement to be executed on the same line of written code.
               -Example from the project:
               
               // Lines 255 - 256
               if (bally == height - 1)
                  ball->changeDirection(ball->getDirection() == DOWNRIGHT ? UPRIGHT : UPLEFT);
               
               // Breaking lines 255-256 apart, transforming from 2 lines of code to 7 lines.
               if (bally == height - 1)
               {
                  if (ball->getDirection() == UPRIGHT)
                      ball->changeDirection(DOWNRIGHT);
                  else
                      ball->changeDirection(DOWNLEFT);
               }      
               

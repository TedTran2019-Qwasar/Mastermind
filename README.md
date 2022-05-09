# my_mastermind

My implementation of the Mastermind game. 

-c specifies the secret code, otherwise it'll be randomly generated.
-t specifies the number of attempts, otherwise it'll be 10 by default. 

Example of valid inputs:
1. ./my_mastermind 
2. ./my_mastermind -c 0123 [Any non-4 digit code will return invalid input.]
3. ./my_mastermind -t 2147483647 [Input < 1 or Input > 2147483647 will be invalid]
4. ./my_mastermind -c 0123 -t 2147483647
5. ./my_mastermind -c 0123 -c 1111 -c 2222 -t 11 -t 12 -c 2222

Once gameplay has started, enter 4 numbers ranging from 0-7.
1. "1234" is valid input, "8899" is invalid input, "01234" is invalid

To compile: make
Use leaks -atExit -- ./my_mastermind to check for memory leaks.

If you're testing on Qwasar's platform, I have no idea. It seems like they don't 
have Valgrind or Leaks pre-installed, so possibly try -fsanitize=address -fno-omit-frame-pointer 
while compiling and look up LeakSanitizer's documentation on Github.
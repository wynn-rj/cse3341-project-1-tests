# cse3341-project-1-tests
Test cases for cse3341 project 1

error cases 1-5 and pass cases 1-4 have been provided by the professor and are 
included in here for ease of use

## Using autotest
`autotest` can run your interpreter against all the test cases. The
autotester is invoked as below:
```
./autotest <interpreter> [--verbose|--error]
```
The interpreter argument is how to run your interpreter, if your interpreter
is a compiled binary then this can be run as 
```
./autotest path/to/interpreter
```
If your interpreter is a python program then it can be run as
```
./autotest "python3 path/to/interpreter.py"
```
The optional flags must be specified at the end. If the `--verbose` flag is set 
the autotester will print the interpreter output for all test cases instead of
suppressing it. If the `--error` flag is specified the error recieved in the 
error cases will be printed. This is useful for checking that your error values
are correct

## Creating test cases
Each test is defined by a folder in the `pass-cases` or the `error-cases` 
folders. The name of the folder can be arbitrary, but it will be used to 
identify the test when running the automated tester unless a 
[name file](#name-files) is included.

Each test cases requires a `test.data` file and a `test.code` file. If the case 
is expected to succeed it should be places in the `pass-cases` folder, otherwise
the test should be placed in the `error-cases` folder. Additionally, for all 
passing tests, a `test.expected` file should be placed with the test.

### Name files
With each test a `test.name` file can be specified to replace the 
folder name standardly used by the automated tester. The contents of the file 
will be used as the name of the test case

### Help files
With each test a `test.help` file can be specified that contains text to help
explain how to fix the interpreter if the case were to error

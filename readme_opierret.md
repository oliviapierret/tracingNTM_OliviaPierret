# Project Tracing NTM Behavior Readme Team OliviaPierret

| 1 | Team Name: OliviaPierret |
| :---: | ----- |
| 2 | Team members names and netids: Olivia Pierret, opierret |
| 3 | Overall project attempted, with sub-projects: Program 1: Tracing NTM Behavior |
| 4 | Overall success of the project: Completed successfully |
| 5 | Approximately total time (in hours) to complete: 5 |
| 6 | Link to github repository: [https://github.com/oliviapierret/traceTM\_OliviaPierret](https://github.com/oliviapierret/traceTM_OliviaPierret) |
| 7 | List of included files (if you have many files of a certain type, such as test files of different sizes, list just the folder): (Add more rows as necessary). Add more rows as necessary. File/folder Name File Contents and Use Code Files [trace\_NTM\_OliviaPierret.py](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/trace_NTM_OliviaPierret.py) Uses given machine information and input strings to trace all possible paths the NTM could take. Outputs the results to the output file that contains the name of the machine, input string, how many transitions it took for the string to be accepted/rejected, the degree of nondeterminism, and the trace path for each input string. [data\_NTM\_description.csv](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/data_NTM_description.csv) A csv that includes information about the machine: Line 1: Name of machine Line 2: List of state names for Q Line 3: List of characters from Σ Line 4: List of characters from Γ Line 5: The start state Line 6: Accept state Line 7: Reject state Lines 8 \- 10: Possible transitions to accept state [termination\_flag.csv](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/termination_flag.csv) Only includes the termination flag (number) that will stop execution if the total number of transitions simulated exceeds the number (15). Test Files [check\_strings.csv](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/check_strings.csv) This csv contains all of the input strings I used for testing, including some that reach an accept state and some that don’t. Output Files [output\_data.txt](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/output_data.txt) A text file that contains the output returned from [trace\_NTM\_OliviaPierret.py](https://github.com/oliviapierret/traceTM_OliviaPierret/blob/main/trace_NTM_OliviaPierret.py)  Plots (as needed)  |
| 8 | Programming languages used, and associated libraries:  Python: csv |
| 9 | Key data structures (for each sub-project): classes, dictionaries, lists, sets, tuples |
| 10 | General operation of code (for each subproject):  The NTM class is initialized with the machine file, which contains the description of the NTM's states, symbols, and transitions. The load\_machine method reads the csv file and loads the machine's description into variables. The process\_string method initializes the tape with the input string and starts with the initial configuration then explores the next possible configurations using a breadth-first search approach. It pops a configuration from the front of the queue and processes it. For each configuration, it checks if it has been visited before to avoid cycles. If the current state is the accept state, the machine accepts the input, and the simulation stops, writing the results to the output file. If the current state is the reject state, the machine rejects the input. If no acceptance or rejection occurs, the code proceeds to apply the possible transitions for the current state and symbol, which are fetched from the transitions dictionary. This continues until the machine reaches an accept state, reject state, or the number of steps exceeds a maximum threshold.  |
| 11 | What test cases you used/added, why you used them, what did they tell you about the correctness of your code. I included 4 strings that I knew were correct to make sure they ended in accept states, each varying in length to make sure it would work for longer and shorter strings. I drew a state machine and wrote out the expected trace output to make sure that matched as well. I then put 2 test cases that I knew were not a part of the language so I could make sure it rejected both of those, which it did. I also included one test case that exceeded the number of max transitions to make sure that feature worked correctly. Everything worked as expected, which allowed me to verify the correctness of my code. |
| 12 | How you managed the code development: First I picked a regular expression (a+b\*) and created the csv of machine information to represent it. I then created the NTM class and parsed the information. The rest of the logic for the actual trace I mapped out in my head then started coding. It took some guessing and checking but I was able to debug it and check with the test cases. |
| 13 | Detailed discussion of results:  Each test demonstrates the NTM’s ability to handle different cases, including just ‘a’, just ‘ab’ and multiple a’s followed by multiple b’s. The code also demonstrates the ability to reject strings that are not in the language. The longer the string, the more possible transitions there are so the trace becomes longer. The results demonstrate nondeterminism because you can see the different paths that the machine explores for each of the strings. |
| 14 | How team was organized: I worked individually |
| 15 | What you might do differently if you did the project again: I would make a better plan going in, I just started writing without much of a plan and had to pretty much restart. |
| 16 | Any additional material: None |



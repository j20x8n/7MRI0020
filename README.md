java c
7MRI0020 Scientific programming - Year 2024/2025 
Coursework 2
This coursework mark contributes 60% of your final mark   for this   module
This coursework will cover topics covered in the second   half of the   module,   in   particular:
-            Testing   (Task   1)
-            Algorithm and complexity   (task 2)
-            Concurrency and native   language   (task 3)
The topic of this coursework will be the Development of a software tool to split an image from top to bottom based on lowest change of intensities 
Your implementation will be assessed using the following   considerations:
-            functionality of the code (does   it work?),
-            your use of language features   (idiomatic   python),
-          the quality of your comments and   your   adherence   to formatting standard,
-          the efficiency   of the   implementation,   both   in term   of   computation   and   memory   usage.Finally, it should be noted that this is an   individual   project, and your   code will   be   automatically   checked for plagiarism and collusion.   In the event, plagiarism is detected, you will be reported   for miss-conduct. You can find more information   about the   relevant   processes   on this page.You   are   expected   to   submit   a   single   zipped   folder   containing   only   three   python   files   named   main.py, squareimage.py and    test_squareimage.py. This should   be submitted via the   dedicated   Keats   submission   section   on   the   7MRI0020   module   page,   where   the   deadline   is   specified. Your submission should be anonymised, so do not include any identifiable   information in the filename of the notebook   nor   in your code.The   aim   of this   coursework   is to   create   a software tool to   detect   the   path   which   links   the   top   of an   image   (any   pixel from the top   row) to   the   bottom   (any   pixel   from   the   bottom   row)   while   minimising the overall absolute intensity differential on   the   path.
Starting from a 2D grid, we aim to establish a path   that   links   any   pixel from   the   top   row   to   any   pixel from the bottom row while satisfying these   conditions:
-             (Condition   1) A given   pixel on a   row   (red)   can   only   be   connected   to the pixel under it on the following row or   the two voxels on   either   side of the central one (blue),   as   illustrated   beside.

-            (Condition   2)   The   sum   of   absolute   differential   value   between   all   pixels on the path should be minimal. For example, the total value   associated   with   the   path   highlighted   in   blue   (2-4-2-1-5)   on   the   right-hand side figure would   be computed   as:
|2-4|   +   |4-2|   +   |2-1|   +   |1-5|
Note    that    the    path      shown      is      not      the      optimal      solution      to      the   problem.
Task    1    [40    marks]: The   provided   code   implements   a   naive   approach   that   evaluates   all   possible    solutions    (brute    force)    for    a    square    image    and    returns    a    best      solution    for    the   aforementioned task.The   provided `find_minimal_path_brute_force`   method lacks   modularity and   is   hard to validate   as   it   implements   all   required functionalities to   extract the   best   path.   Rewrite the   components   of          代 写7MRI0020 Scientific programming - Year 2024/2025 Coursework 2Python
代做程序编程语言   this                method                into             multiple                methods                instead.                You             should                call                the   `find_minimal_path_alternative`   method instead of `find_minimal_path_brute_force`.
Ensure   all   methods you   add,   including   `find_minimal_path_alternative`,   are thoroughly tested.   Create a file `test_squareimage.py`   to implement your unit tests   using   the   `unittest`   module.
For example, the following function:
def large_function(): 
a = np.random.randint(10) b = a * 10 c = b ** 2 return c 
should be changed   into the following:
def routineA(): 
return np.random.randint(10) 

def routineB(v): 
return v * 10 

def routineC(v): return v**2 

def split_function(): a = routineA() b = routineB(a) c = routineC(b) return c 
where the `routineA`, `routineB`, `routineC` and `split_function` functions   should   be tested.
Note:
-          The `find_minimal_path_brute_force`   method   is   not to   be   altered,
-          You are   not   expected to write   unit   tests   for   the   other   provided   methods,
-          You   should write   as   many   tests   as   you   think   are   required,
-            You can write both   positive and   negative tests.
Marking scheme:
-            Overall code presentation (organisation, comments, …) [5]
-               Working solution   [5]
-             Appropriate re-organisation of the original   method   [5]
-            Appropriate sets of unit tests   [25]
Task 2 [30 marks]: Implement a non-brute force approach (recursive, dynamic, divide and conquer, greedy, randomised, other) to efficiently solve the problem. Your approach should be called by the `find_minimal_path_optimised` method.
Marking scheme:
- Overall code presentation (organisation, comments, …) [5]
- Significant speedup [15]
- Working alternative approach [10]
Task 3 [20 marks]: In the method find_minimal_path_accelerated`, accelerate further your non-brute force approach using multi-threading and/or native language (as per Week 9 content). Note that should you have encounter issues with Task 2, you can accelerate the provided brute force approach. Note as well that depending on your Task 2 implementation, the obtained additional speed-up could be limited. In less than 200 words, comment and explain the obtained acceleration. You answer should be added as comment in the squareimage.py file.
Marking scheme:
- Overall code presentation (organisation, comments, …) [5]
- Significant speedup and/or appropriate justification [10]
- Working approach [5]
Task 4 [10 marks]: Decorate all methods listed below to display information about the approach and time it takes to extract the path. The following methods should be decorated:
- `find_minimal_path_brute_force`
- `find_minimal_path_alternative`
- `find_minimal_path_optimised`
- `find_minimal_path_accelerated`
For example, the text displayed after running the `find_minimal_path_alternative` method should read: `The alternative approach ran in n second(s)`, where `n` is replaced by the time it took in second with two decimals to represent floating values.
Marking scheme:
- Working decorators and appropriate display [5]
- Single function to decorate all methods [5]



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com

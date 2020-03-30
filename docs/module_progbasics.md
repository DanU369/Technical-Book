# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!
---A list is used to store more elements in a single variable so you can further modify and iterate through them. Some examples of methods used for lists are:
list.append(element)=add the 'element' at the end of the 'list'
list.remove(thing)=searches the 'list' and remove the first element='thing'
list.pop(index)=remove the element  from the 'list' at 'index' position and also returns that value

#### What is the difference between a list/array and a set?
---Lists and sets are very similar but the difference is that a set can't contain more than one elements that are identical.

#### What is the purpose and methods of a dictionary/map data structure?
---A dictionary is used to store groups of elements. They have keys(a single element) that corespond to their values(can be any type of data structure. Some example of methods used for dictionaries are:
dictionary.Add(key,value)= adds a group consisting of 'key' and 'value' at the end of the dictionary
dictionary.Remove(key)= removes the group with the key='key' from the dictionary

### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
def fibonacci(n):

    a = 1
    b = 0
    count = 0
    print(a)
    while count < n:
        c = a + b
        print(c)
        b = a
        a = c
        count += 1
 
    
#### How do you find a max value in a list/array if you can’t use any built-in functions?
'''
maximum=0
for item in list:
  if item>maximum:
    maximum=item
  return maximum
'''
#### How do you find the average of values in a list/array if you can’t use any built-in functions?
'''
sum=0
items_no=0
for item in list:
  sum+=item
  items_no+=1
return sum/items_no
'''
#### What do we call an *in-place* sort?
We call _sort()_ an in-place method because it modifies a given list in-place (it modifies the actual list on the spot without returning a new one) by using _<_ comparisons between items.

#### Explain an algorithm which sorts a list!
def bubble_sort(lista):                   #define a function called bubble_sort that takes 1 argument lista wich is a list of integers
    finnished = False                     #define a variable to check if we finnished the sorting
    while not finnished:                  #repeat until the sorting is not finnished
        for index in range(len(lista)-1): #iterate through the indices of the list
            finnished = True              #the iteration is finnished if the function doesen't go through the next if
            if lista[index] > lista[index+1]: #check if one element is greater than the next
                lista[index], lista[index+1] = lista[index+1], lista[index] #if it is then swap their places
                finnished = False                     #the iteration is not finished
    return lista                  #return the sorted list
      
    


### Programming paradigms - procedural

#### What is the call stack?
A call stack is a stack data structure that stores information about the active subroutines of a computer program.
The call stack is what a program uses to keep track of method calls. The call stack is made up of stack frames—one for each method call.

#### What is “Stack overflow”?
In software, a stack overflow occurs if the call stack pointer exceeds the stack bound. The call stack may consist of a limited amount of address space, often determined at the start of the program.

#### What are the main parts of a function?
The main parts of a function are:
1.Keyword def marks the start of function header.
2.A function name to uniquely identify it. Function naming follows the same rules of writing identifiers in Python.
3.Parameters (arguments) through which we pass values to a function. They are optional.
4.A colon (:) to mark the end of function header.
5.Optional documentation string (docstring) to describe what the function does.
6.One or more valid python statements that make up the function body. Statements must have same indentation level (usually 4 spaces).
7.An optional return statement to return a value from the function.

### Programming languages - Python  
#### How do you use a dictionary in Python?
A dictionary contains elements in form of pairs key:value. You can use dictionaries to acces a certain data (values) by the key.

#### What does it mean that an object is immutable in Python?
If a object is immutable you can't modify it(add, delete,update).

#### What is conditional expression in Python?
Conditional expressions contain a block of code that is executed only if the statement is True
Those expressions are:
if "condition": If "condition" is True it will execute what is indented under it
elif: If the if condition is not True then this condition is verified and if it's True it will execute what is indented under it
else: If all the others conditions are not True then it will execute what is intended under it.

#### What are different types of arguments in Python?
1. Default arguments: (argmunet=value) if an argument is not given then the value is used as an argument
2. Keyword arguments: (a=1,b=2) if we can put instead (b=2,a=1) and the function gives us the same result then those are keyword arguments.
3. Arbitrary arguments: (*argument) You may not always know how many arguments you’ll get. In that case, you use an asterisk(*) before an argument name.

#### What is variable shadowing? (context: variable scope)
Variable shadowing occurs when a variable declared within a certain scope (decision block, method, or inner class) has the same name as a variable declared in an outer scope.

#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
If you iterate through the lenght of the list you can encounter various errors like index out of range or elements missed during iteration
#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
The "golden rule" of variable scoping in Python (context: LEGB, L = Local, E = Enclosed (function is wrapped inside another function), G = Global, B =Built-in): when local as well as global variable is present, *preference is given to the local variable*. 
The lifetime of a variable: it exists for as long as the function is executing. 
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
* The built-in Python function _iter()_, which returns something called an iterator. The built-in function _next()_ is used to obtain the next value from an iterator:
```
a = ['foo', 'bar', 'baz']
itr = iter(a)
next(itr)
next(itr)
next(itr)
```
* If all the values from an iterator have been returned already, a subsequent next() call raises a StopIteration exception. 
#### What type of elements can a list contain in Python?
A list can contain any type of elements.
#### What is slice operator in Python and how to use?
* The slice operator is a method that extracts a subset of a list, which will itself be a list.
* In order to use it, you need to specify an upper and lower bound. Note that our sublist will include the element at the lower bound, but _exclude_ the element at the upper bound:
'''
animals = ['cat', 'dog', 'fish', 'bison']
print(animals[1:3]) # ['dog', 'fish']
print(animals[1:-1]) # ['dog', 'fish']
'''
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
"+" you can use addition to merge 2 lists into 1 list with both elements
"*" you can use multiplication with one list in form of (list*integer) to form a list that contains the element from the initial list "number" number of times

#### What is the purpose of the in and not in membership operators in Python?
Operators like IN and NOT IN are used to validate if an element is contained by a sequence (list, string, tuples...)

#### What does the + operator mean when used with strings in Python?
If the "+" operator is used on 2 strings it will merge them into 1 containing the first string folowed by the second one. 

#### Explain f strings in Python?
f strings are the fastest way to format a string. Beforehand you must define variables and then use those variables where you want them to use between {}.
'''
ex:
name=Dan
f'Hello, {name}!'
OUTPUT: Hello, Dan!
'''
#### Name 4 iterable types in Python!
Strings, lists, tuples, dictionaries

#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
They are similar but the generator has a lower memory size allocation. Also you can't access individual elements by index.

#### Does the order of the function definitions matter in Python? Why?
The only thing that matters is that the function definition must be before function call. 

#### What does unpacking mean in Python?
There are 2 ways of unpacking:
'''
my_list = ["one", "two", "three"]
print(*my_list)
OUTPUT: one two three

my_dict = {"name": "Jane", "surname": "Doe"}
print(*my_dict)
OUTPUT: name surname
print(**my_dict) #should be used as keyword arguments
Output: TypeError: 'a' is an invalid keyword argument for this function
def func(a,b):
  print(a,b)
func(**my_dict)
OUTPUT: Jane Doe
'''
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
The variable will have the value None

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
You can run the debug in vSC to see what the program does after each step
You can use print() statements to see if the program enters the desired block of code

#### What does step over, step into and step out mean while using the debugger?
Step over skips the next function from debugging steps
Step into enters the next function and execute it step by step
Step out end the debugging of the current function and go to the next one

#### How can you start to debug a program from a certain line using the debugger?
You must place a break point (turn the grey dot next to line number to red)

### Version control

#### What are the advantages of using a version control system?
The primary benefits you should expect from version control are as follows:
    1. A complete long-term change history of every file (enables going back to previous versions to help in root cause analysis for bugs and it is crucial when needing to fix problems in older versions of software).
    2. Branching and merging. Individuals working on their own can benefit from the ability to work on independent streams of changes. There are many different workflows that teams can choose from when they decide how to make use of branching and merging facilities.
    3. Traceability. Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.
#### What is the difference between the working directory, the staging area and the repository in git?
Git has 3 areas:
    + The _working directory_ = contains the latest downloaded version from the repository together with any changes that have yet to be committed. As you're working on a project, all changes are made in this working directory.
    + The _staging area_  = helps to maintain this workflow by allowing you to only promote certain files at a time instead of all the changes in your working directory. Users move, otherwise referred to as promote, changes from the working directory, to a staging area before committing them into the repository.
    + The _repository_ = a virtual storage of your project. It allows you to save versions of your code, which you can access when needed.
#### What are remote repositories in git?
Remote repositories are versions of your project that are hosted on the Internet or network somewhere. Collaborating with others involves managing these remote repositories and pushing and pulling data to and from them when you need to share work.
#### Why does a merge conflict occur?
Merge conflicts happen when you merge branches that have competing commits, and Git needs your help to decide which changes to incorporate in the final merge.
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
In Terminal, add the URL for the remote repository where your local repository will be pushed:
    + $ git remote add origin remote repository URL # Sets the new remote
    + $ git remote -v # Verifies the new remote URL
- Push the changes in your local repository to GitHub:
    + $ git push origin master # Pushes the changes in your local repository up to the remote repository you specified as the origin
#### What does it mean atomic commits and descriptive commit messages?
When making code changes, you want to make commits that are generally smaller and that encompass only one irreducible feature, fix, or improvement.
#### What’s the difference between git and GitHub?
Git is a version control system that lets you manage and keep track of your source code history.
- GitHub is a web-based hosting service that lets you manage Git repositories.  If you have open-source projects that use Git, then GitHub is designed to help you better manage them.

## Software design

### Clean code

#### What does clean code mean?
A clean code means you have no dead code(code that doesn't affect your result), the least amount of global variables, functions for repeating actions, variables and functions have descriptive names easy to understand, comments if necessary

#### What steps do we usually do during a clean code refactoring?
Make sure that the above steps are done

### Error handling

#### What is exception handling?
The use of try and except. So if an error is happening it will not break the program and instead execute a different piece of code.
#### What are the basics of exception handling in Python?
- The basics of _exception handling_ consist of _try-except_ blocks. Python will try to process all the statements inside the _try_ block. 
- If an error occurs at any point as it is executing them, the flow of control will immediately pass to the except block, and any remaining statements in the try block will be skipped.
- It is good practice if the only code inside the try block is the single line that is the potential source of the error that we want to handle.

#### In which case should we catch an exception? Why?
In case we want to protect a piece of code against some errors.
In case we have to do different things for different types of data.
We ca also use it to limit user's input.

#### What can/should we do with an exception in the ‘except’ block?
We can write different pieces of code that are executed for different errors.

#### What does the else and finally statement do in a try-except block in Python?
- The _else_ statement will be executed only if the try clause doesn’t raise an exception.
- The _finally_ clause will be executed at the end of the try-except block no matter what – if there is no exception, if an exception is raised and handled, if an exception is raised and not handled, and even if we exit the block using *break*, *continue* or *return*. We can use the *finally* clause for cleanup code that we always want to be executed.

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?
Code can be written in many forms with the result being the same. So getting another opinion or a different perspective on the code you written helps alot. Maybe there was a shorter, simpler way that you didn't think of.
As a team a retrospective meeting shows the strong and the weak points of the team. And leaves room for improvement 

## Programming environment

### Unix

#### What is UNIX and what is Linux?
- UNIX is an operating system that was born in the late 1960s, when AT&T Bell Labs released an operating system called Unix written in C, which allows quicker modification, acceptance, and portability. It began as a one-man project under the leadership of Ken Thompson of Bell Labs. It went on to become most widely used operating systems. Unix is a proprietary operating system. Unix is a proprietary operating system.
- Linux is a replica of UNIX that does not use its code built by Linus Torvalds at the University of Helsinki in 1991. The name "Linux" comes from the Linux kernel. It is free and open source software.

#### What do we call the shell in Linux?
Shell = command line interpreter/terminal

#### What does root means in a Linux environment?
- Root is the user name or account that by default has access to all commands and files on a Linux or other UNIX-like operating systems. It is also referred to as the root account, root user and the superuser.

#### How do you access your personal files in Linux?
- In Linux, personal data is stored in /home/username folder.

#### How can you install an application in Linux?
- Run the command in the Terminal (text input/output environment):
sudo apt install <name_of_application>

#### What is package management in Linux, what are repositories?
- Package management system allows users to install, update, remove and get information about software installed.
- Repositories are storage locations where the packages are downloaded from.
- Users can use _apt_ and _dpkg_ commands to query and update the database of software available in repositories and installed on the system, to install or remove software and upgrade installed packages, and clean up obsolete programs.

#### How do you navigate in the filesystem with the command line?
- _cd_ Change directory. Used to navigate between folders.
- _pwd_ Display current directory.
- _ls_ Display a list of files in the current directory.
- _stat_ Display when a file was last accessed, modified, or changed.

#### What does the following commands do: mkdir, rm, cat, cp, touch?
- _mkdir_ Create a directory.
- _rm_ Remove a file or set of files.
- _cat_ Display the contents of a text file.
- _cp_ Makes a copy of a file.
- _touch_ Create a file.

#### How can you look up what does a command do in Linux if you have no internet connection?
- _command --help_ or _man command_

#### What does the following commands do: head, tail, more, less?
- _head_ Output the first 10 lines of file.
- _tail_ Output the last 10 lines of file.
- _more_ Output the contents of file.
- _less_ View and paginate file.

#### How do you download a file from internet using the terminal?
- _wget file_

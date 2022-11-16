# Simple Shell
> In this project, we coded from scatch a simple Unix shell. A shell is an interactive
> command-line interpreter. We created a shell that would utilize the command line
> interface (CLI). It allows users to type in a defined set of
> commands (e.g. "rm" to remove files, "cat" to combine word documents, etc) and have the
> operating system run the appropriate function. It is slightly different from a graphical user
> interface (GUI).
> A user can create/write/read/open/remove folders, print things to the terminal, change directories, print where you are
> in the system, etc. 

### Synopsis
> This repository holds all the code necessary for our custom simple shell to run.
> Our shell currently handles the executions of executables found in the
> environmental variable PATH, with or without their full paths. Sample commands
> that our shell supports include ```ls``` (```/bin/ls```), ```pwd```, ```echo```,
> ```which```, ```whereis```, etc. We've also created the following builtins.


### Builtins
* ```exit``` exits shell (```Usage: exit [status]```)
* ```env``` prints environmental variables (Usage: ```env```)
* ```setenv``` creates or modifies an environmental variable (Usage: ```setenv name value```)
* ```unsetenv``` removes an envrionmental variable (Usage: ```unsetenv name value```)
* ```cd``` changes directories (Usage: ```cd [-][~][path]```)

### Functions and system calls used
```read```, ```signal```, ```malloc```, ```free```, ```getcwd```, ```chdir```, ```access```, ```execve```, ```wait```, ```write```,  ```exit```

### Description of what each file shows:
```
man_3_shell ------------------------ custom manpage for our simple shell
main.c ----------------------------- holds entrance into program
shell.h ---------------------------- holds prototypes of functions spread across all files
```
Helper files
```
prompt.c --------------------------- handles outline of shell's reprompting and executing
non_interactive.c ------------------ handles output when shell is called outside of shell
_realloc.c ------------------------- helper function handles reallocation
_strcat.c -------------------------- concatenates two strings
_strcmp.c -------------------------- compares if two strings match
_strcpy.c -------------------------- copies a string
_strdup.c -------------------------- duplicates a string
_str_tok.c -------------------------- (custom) tokenizes user's command input and returns array
c_str_tok.c ------------------------- tokenizes PATH to include ":" as Null, checks current dir
get_line.c ------------------------- (custom) reads user's typed input into buffer
_which.c --------------------------- appends command to PATHs, fleshes paths out, returns match
_cd.c ------------------------------ changes directories
linked_lists.c --------------------- adds and deletes nodes; prints and frees linked list
get_env.c -------------------------- finds and returns copy of environmental variable
env_linked_list.c ------------------ prints and creates linked list of envrionmental variables
set_unset_env.c -------------------- finds environment variable index node, sets and unsets
free_double_ptr -------------------- frees double pointers (user's command, arrays)
_execve.c -------------------------- executes and frees command, then exits program
__exit.c --------------------------- handles if user types exit or exit(value)
int_to_string.c -------------------- converts int to string to write error messages
print_error.c ---------------------- prints special error messages for certain fails
```
### Environment
* Language: C
* OS: Ubuntu 14.04 LTS
* Compiler: gcc 4.8.4
* Style guidelines: [Betty style](https://github.com/holbertonschool/Betty/wiki)

### How To Install & Compile
```
$ git clone git@github.com:selma-belhadj/simple_shell.git
$ cd simple_shell
$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
$ ./hsh
```
## Authors

👤 **Selma Belhadj**

- GitHub: [@selma-belhadj](https://github.com/selma-belhadj)
- Twitter: [@Bel_Selma16](https://twitter.com/Bel_Selma16)
- LinkedIn: [@selma-belhadj](https://www.linkedin.com/in/selma-belhadj/)

👤 **Kanu Mike Chibundu**

- GitHub: [@Ginohmk](https://github.com/Ginohmk)
- Twitter: [@michotall95](https://www.twitter.com/michotall95)
- LinkedIn: [@kanumike](https://www.linkedin.com/in/kanu-mike-497119211/)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](https://github.com/selma-belhadj/printf/issues).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

## 📝 License

This project is [MIT](./MIT.md) licensed.
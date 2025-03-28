# vi/vim

There are a few modes: _**insert**,_ _**normal** and **command**_ mode.

### Normal mode (navigation)

Press the `esc` button from any other mode. This is the default mode.

### Insert mode (typing & editing)

Press `i` from the normal mode. This mode allows us to directly insert and edit text —  just like a normal text editor.

### Command mode (executing commands)

Press `:` from the normal mode. This mode allows us to run several commands without leaving the editor.  One feature I really appreciate is the ability to run shell commands — see below for more details.

#### Useful commands

1. Save (write) file

```vim
:w  
```

2. Quit

```vim
:q
```

3. Combine write + quit

```vim
:wq
```

4. Quit without saving

```vim
:q!
```

5. Execute shell commands

```vim
:!
:! ls
```

_**Note**_: The symbol `%` represents the current filename without any extensions

#### Examples

Eg. Compile and execute a C program file `test.c` (that is currently opened)

```vim
:! gcc test.c -o test && ./test
:! gcc %.c -o % && ./%
```

Eg. Execute a Python program file `test.py` (that is currently opened)

```vim
:! python3 test.py
:! python3 %.py
```

Eg. Change permissions and execute a `.sh` (shell) script `test.sh`

```vim
:! ls -l
:! chmod +x test.sh
:! ./%
```


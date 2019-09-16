# GDB

* ☐ clean up

| !cmd                       | !desc                                                   |
|----------------------------|---------------------------------------------------------|
| !controlling execution     |                                                         |
| r *arg1 ...*               | run program                                             |
| s                          | step through program                                    |
| si                         | step one instruction exactly                            |
| c                          | continue running program                                |
| !breakpoints               |                                                         |
| b *funcname (or line)*     | set breakpoint at function                              |
| ! ...                      |                                                         |
| bt                         | backtrace                                               |
| l                          | list surrounding source                                 |
| info locals                | show local variables                                    |
| info args                  | show arguments                                          |
| up/down *n*                | go up or down n frames in the stack                     |
| disassemble                | disassemble section of memory                           |
| p/x *variable*             | print variable in hexadecimal                           |
| x *addr*                   | Examine memory at addr                                  |
| show env                   | Show environment                                        |
| set env FOO = bar          | Set environment variable FOO to bar                     |
| whatis *variable*          | show variable type                                      |
| set var *variable=value*   | Set variable to value                                   |
| set env *variable=value*   | Set environment variable to value                       |
| attach *pid*               | Attach gdb to already running process                   |
| set print pretty on        | pretty print structures                                 |
| set print array on         | readable array output                                   |
| set print array-indexes on | show array indices                                      |
| set print demangle on      | demangle C++ names                                      |
| info registers             | show registers (excluding floating point)               |
| macro expand *macro*       | expands a macro (requires -gdwarf-2 -g3 compiler flags) |

| code | print type   |
|------|--------------|
| x    | hexadecimal  |
| u    | unsigned int |
| d    | signed int   |

Check a core dump



 gdb executable coredump

Extensions

<http://rr-project.org/>

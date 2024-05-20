# GDB Cheatsheet

General set-up:
| Command | Description | Shorthand |
| ----------- | ----------- | ----------- |
| `gdb <executable>` | Start GDB session ||
| `list` | Display full source code (if available) | `l` |
| `list N,M` | List source code from line `N` to line `M` (if available) | `l N,M` |
| `break N` | Set breakpoint at line `N` | `b N` |
| `break <label>` | Set breakpoint at `label` | `b <label>` |
| `delete N` | Delete breakpoint number `N` | `d N` |
| `info break` | Show all breakpoints | `i b` |
| `info registers` | Show value of all registers | `i r` |
| `info registers eax` | Show value of `eax` only | `i r eax` |


Run & debug:
| Command | Description | Shorthand |
| ----------- | ----------- | ----------- |
| `run` | Run program ||
| `next` | Advance to next line of execution | `n` |
| `nexti` | Advance to next machine instruction rather than line of source code | `ni` |
| `step` | Step into the next line executed in any subroutine | `s` |
| `continue` | Run to next breakpoint | |
| `until` | Run until next instruction | |
| `finish` | Run until selected stack frame returns | |

Examine:
| Command | Description | Shorthand |
| ----------- | ----------- | ----------- |
| `info locals` | Show values of local vars ||
| `print <variable>` | Show value of specified variable | `p <variable>` |
| `where` or `backtrace` | Show callstack | `bt` |
| `where full` or `backtrace full` | Show callstack & local vars ||
| `info args` | Show args to current func in callstack ||
| `info threads` | Show all threads ||
| `info signals` | Show all signals and how they are handled ||
| `info frame` | Show current frame ||




### Sources
[GDB: The GNU Project Debugger](https://www.sourceware.org/gdb/) \
[pwndgb](https://github.com/pwndbg/pwndbg)

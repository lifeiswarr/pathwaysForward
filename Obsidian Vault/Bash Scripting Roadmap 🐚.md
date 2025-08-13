# [[VANITY]], [[topics to cover]], 

## 🟢 Phase 1: Basics of Bash
- [ ] Understand what Bash is and where it is used
- [ ] Learn how to access the shell (terminal, tty, ssh)
- [ ] Run your first bash script using `./script.sh` and `bash script.sh`
- [ ] Understand file permissions (`chmod +x`)
- [ ] Shebang (`#!/bin/bash`) and its role

## 🟡 Phase 2: Basic Scripting Constructs
- [ ] Variables: defining, using, and scope
- [ ] Echo, printf, and comments
- [ ] Read input from the user
- [ ] Command substitution: `$(...)` and `` `...` ``
- [ ] Arithmetic operations using `$((...))`

## 🟠 Phase 3: Control Flow
- [ ] Conditional statements: `if`, `elif`, `else`
- [ ] Logical operators: `&&`, `||`, `!`
- [ ] Loops:
  - [ ] `for` loop
  - [ ] `while` loop
  - [ ] `until` loop
- [ ] Loop control: `break`, `continue`
- [ ] Case statements: `case...esac`

## 🔵 Phase 4: Functions and Parameters
- [ ] Define and call functions
- [ ] Function parameters: `$1`, `$2`, ...
- [ ] Return values and `exit` status
- [ ] Local vs global variables inside functions

## 🟣 Phase 5: Working with Files and Text
- [ ] Redirect output: `>`, `>>`, `<`, `2>`, `&>`
- [ ] Pipes (`|`) and filters (`grep`, `cut`, `awk`, `sed`)
- [ ] Working with `find`, `xargs`, `sort`, `uniq`, `tee`
- [ ] Reading files line by line
- [ ] Writing logs to files

## 🔶 Phase 6: Command Line Arguments and Options
- [ ] `$@`, `$#`, `$*`, `$?`, `$0`
- [ ] Handling flags and arguments
- [ ] Use `getopts` to parse options
- [ ] Create help menu in your scripts

## 🟤 Phase 7: Advanced Bash Scripting
- [ ] Arrays and associative arrays
- [ ] String manipulation and regex
- [ ] Traps and signal handling (`trap`, `SIGINT`, `SIGTERM`)
- [ ] Scheduling jobs with `cron`
- [ ] Background and foreground processes: `&`, `jobs`, `fg`, `bg`
- [ ] Process management: `ps`, `kill`, `wait`

## 🧩 Phase 8: Bash + System Interaction
- [ ] Environment variables (`export`, `.bashrc`, `.bash_profile`)
- [ ] System info (CPU, memory, disk) using Bash
- [ ] Network utilities: `ping`, `curl`, `wget`, `netstat`, `ss`
- [ ] Interacting with system services (`systemctl`, `service`)
- [ ] Working with users and permissions (`sudo`, `groups`, `id`)

## 🧪 Phase 9: Testing, Debugging, and Optimization
- [ ] Use `set -x` and `set -e` for debugging
- [ ] Use `bash -n script.sh` to check syntax
- [ ] Profile scripts with `time`, `strace`
- [ ] Write unit tests with `bats`
- [ ] Optimize loops and commands for performance

## 📦 Phase 10: Projects and Use Cases
- [ ] Build a CLI-based todo manager
- [ ] Automate backups and file organization
- [ ] Monitor server logs and send alerts
- [ ] Build a menu-driven utility (interactive script)
- [ ] Write deployment/CI scripts
- [ ] Create your own `.bashrc` extensions or aliases
- [ ] Automate system maintenance tasks

## 📚 Bonus: Best Practices and Ecosystem
- [ ] Learn shellcheck for linting
- [ ] Follow quoting rules properly (`"$var"` vs `$var`)
- [ ] Always check for command success: `if cmd; then ...`
- [ ] Avoid using `eval` unless absolutely necessary
- [ ] Read advanced Bash sources:  
  - [ ] [Bash Guide for Beginners (TLDP)](https://tldp.org/LDP/Bash-Beginners-Guide/html/)
  - [ ] [Advanced Bash-Scripting Guide](https://tldp.org/LDP/abs/html/)
  - [ ] [ShellCheck](https://www.shellcheck.net/)


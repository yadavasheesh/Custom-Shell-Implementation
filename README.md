🖥️ Custom Shell Implementation

This repository contains a project where I implemented a custom shell environment in C (or whichever language you used).
The goal was to explore system-level programming, process management, command parsing, piping, redirection, and background execution.

📂 Project Overview
Feature	Description
Command Loop (REPL)	Reads user input continuously and processes commands
Built-in commands	Supports commands like cd, exit, history, etc.
External command execution	Launches external programs using fork() + exec() (or equivalent)
Input/Output redirection	Supports <, >, >> to redirect stdin/stdout
Piping (`	`)
Background execution	Supports & at end of command to run process asynchronously
Command History	Stores previously executed commands for reuse (e.g., !!)
🛠 How to Build & Run

Clone the repository:

git clone https://github.com/yadavasheesh/Custom-Shell-Implementation.git


Navigate to the project directory:

cd Custom-Shell-Implementation


Compile the code (example with GCC):

gcc -o my_shell shell.c  # or appropriate source files


Run the shell:

./my_shell


You should see a prompt (e.g., myshell> ), and you can enter commands like:

ls -l
grep foo file.txt | sort
sleep 10 &

🧠 What I Learned

In-depth knowledge of system calls like fork(), exec(), wait(), pipe(), dup2(), and how they work under UNIX-like systems. 
Brennan
+1

How to parse command line input, handle tokens, arguments, and special operators (<, >, |, &)

Managing child processes, handling input/output redirection, and supporting pipelines

Designing a minimal but functional command interpreter — useful for understanding how shells like bash are built 
Computer Science at Purdue

Learning about background process management and asynchronous execution

🎯 Why This Project Matters

This isn’t just a simple script — implementing a shell gives you insight into how operating systems, processes, and commands interact. Many interviewers value this kind of project because it demonstrates low-level understanding, which sets you apart from basic CRUD engineering tasks.

🤝 Contribution & Improvements

Although this project is mainly for personal learning, contributions are welcome. Suggestions might include:

Add support for environment variables ($VAR)

Implement more built-in commands (export, alias, etc.)

Add command line editing, auto-completion, and job-control (background/foreground)

Improve error handling, signal management (SIGINT, SIGCHLD)

⭐ If you find this project interesting or useful, please consider giving it a star.

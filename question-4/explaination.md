1. `lsof -u $(whoami) | head -n 15`
   - **Explanation:** This command displayed the first 15 open files and processes associated with my user **rithwik**. It showed the active processes currently maintaining open file descriptors.

2. `ls -la /proc/$$/fd`
   - **Explanation:** This listed the file descriptors for the current shell session. It confirmed that standard input (0), standard output (1), and standard error (2) are connected to the current terminal.

3. `ls /fake_directory > standard_out.txt 2> error_out.txt`
   - **Explanation:** This attempted to list a directory that does not exist while redirecting standard output and standard error into separate files. The error message was stored in **error_out.txt**.

4. `cat error_out.txt`
   - **Explanation:** This displayed the contents of the error log and confirmed that the standard error stream successfully captured the "No such file or directory" message.

5. `ulimit -a`
   - **Explanation:** This displayed the current shell resource limits, including limits on open files, stack size, memory, and other process resources.

# System and Link Analysis

## Objective

The objective of this task is to understand Linux file linking, file descriptors, input/output redirection, and system resource limits using standard command-line utilities.

---

## Commands Used

### `touch original_file.txt`

Creates an empty file.

---

### `echo "Hello Linux" > original_file.txt`

Writes sample content into the file.

---

### `ln original_file.txt hard_link.txt`

Creates a hard link pointing to the same inode as the original file.

---

### `ln -s original_file.txt sym_link.txt`

Creates a symbolic (soft) link pointing to the original file.

---

### `ls -li original_file.txt hard_link.txt sym_link.txt`

Displays inode numbers and verifies both links.

The hard link shares the same inode as the original file, while the symbolic link references the file path.

---

### `rm original_file.txt`

Deletes the original file.

---

### `cat hard_link.txt`

The hard link continues to provide access to the file contents.

---

### `cat sym_link.txt`

The symbolic link becomes invalid because its target file no longer exists.

---

### `lsof -u $(whoami) | head -n 15`

Displays open files associated with the current user.

---

### `ls -la /proc/$$/fd`

Lists the current shell's open file descriptors.

---

### `ls /fake_directory > standard_out.txt 2> error_out.txt`

Redirects standard error to a separate file.

---

### `cat error_out.txt`

Displays the captured error message.

---

### `ulimit -a`

Shows the current shell resource limits, including file size, memory usage, stack size, and maximum user processes.

---

## Conclusion

The experiment successfully demonstrated the behavior of hard and symbolic links, verified open file descriptors, performed standard error redirection, and inspected system resource limits. The results confirmed the differences between hard and symbolic links and illustrated basic Linux process and file management concepts.

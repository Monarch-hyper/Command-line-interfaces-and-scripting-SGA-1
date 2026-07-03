# Project Workspace and Permission Management

## Objective

The objective of this task is to understand Linux file permissions, ownership, directory creation, and the effect of the `umask` command while organizing a simple project workspace.

---

## Commands Used

### `umask`

Displays the default permission mask used when creating new files and directories.

**Output**

```
0002
```

This configuration allows group members to have write permissions while restricting write access for others.

---

### `mkdir -p project_workspace/docs project_workspace/code`

Creates the project workspace along with the required subdirectories.

---

### `touch project_workspace/docs/design.txt`

Creates an empty file named **design.txt** inside the **docs** directory.

---

### `ls -l project_workspace/docs/design.txt`

Displays the permissions, owner, group, and other details of the created file.

The file was successfully created with the default permissions assigned according to the current umask.

---

### `chmod 700 project_workspace/code`

Changes the permissions of the **code** directory.

Permission **700** provides:

- Read, write, and execute permissions to the owner.
- No permissions to the group.
- No permissions to others.

---

### `chown $USER:$USER project_workspace/docs/design.txt`

Assigns the ownership of the file to the current user and group.

The ownership was successfully verified for user **rithwik**.

---

## Conclusion

The project workspace was created successfully. The default umask value was verified, directories and files were created correctly, directory permissions were modified using `chmod`, and file ownership was confirmed using `chown`. This demonstrates the basic Linux file permission and ownership management process.

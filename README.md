# Linux File Permissions Management Project

## Project Description
This project involves investigating and updating file permissions in Linux to ensure they match the required authorization levels.

## File Permission Checking

### Command Used
```bash
ls -la
```
This command checks permissions of all files in the projects directory, including hidden files.

### Understanding Permission Strings

Example file: `.project_k.txt`  
Permission string: `rw-rw-rw-`

#### Permission String Breakdown:
- First character: No `d` indicates this is a file (not a directory)
- User (Owner) Permissions: `rw-`
  - `r`: Read permission granted
  - `w`: Write permission granted
  - `-`: No execute permission
- Group Permissions: `rw-`
  - `r`: Read permission granted
  - `w`: Write permission granted
  - `-`: No execute permission
- Other Permissions: `rw-`
  - `r`: Read permission granted
  - `w`: Write permission granted
  - `-`: No execute permission

## Permission Modifications

### Regular Files
- Organization policy: Others should not have write access to any files
- Command used:
```bash
chmod a-w project_k.txt
```
This removes write permissions for all users (user, group, and others)

### Hidden Files
File: `.project_x.txt` (archived research file)
Requirements:
- No write permissions for anyone
- User and group should have read access only
- Commands executed to:
  - Remove write permissions for all
  - Add read permission for group

### Directory Permissions
- Location: `drafts` directory
- Owner: `researcher2`
- Requirements:
  - Only `researcher2` should have access
  - Group execute permission removed
- Command used to remove group execute permission

## Summary
The project implemented the following security measures:
1. Initial permission audit using `ls -la`
2. Modified file permissions to remove write access where needed
3. Set archived files to read-only for authorized users
4. Restricted directory access to appropriate users
5. Verified all changes align with organizational security policies

These changes ensure:
- Proper access controls are in place
- Sensitive research data remains secure
- Compliance with organization security policies
- Appropriate user and group permissions



Would you like me to modify any section of the README or add additional information?

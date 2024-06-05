# File System Permissions Management

## Overview

As a security professional at a large organization, your primary responsibility is to ensure the research team has the appropriate permissions on the file system. This helps maintain the security and integrity of sensitive data. This repository contains the scripts and instructions needed to examine and modify file system permissions to match the required authorization levels.

## Objectives

- Examine existing file system permissions.
- Determine if the current permissions match the required authorization.
- Modify permissions to authorize the appropriate users.
- Remove any unauthorized access.

## Scenario

You are tasked with examining the existing permissions on the file system for the research team. If the permissions do not match the required authorization, you will need to modify them accordingly.

## Instructions

### Step 1: Identify the File or Directory

Determine the path of the file or directory to be checked. For example:
```bash
/research_data/project1
```

### Step 2: Check Current Permissions

Use the following command to list the current permissions of the file or directory:
```bash
ls -l /research_data/project1
```
Example output:
```
drwxr-xr-x 2 user1 research_team 4096 Jun  5 12:34 /research_data/project1
```

### Step 3: Determine and Set Appropriate Permissions

Based on the organization's policies, ensure the correct permissions are set. For example, to ensure the owner has read, write, and execute permissions while the group has read and execute permissions:
```bash
chmod 750 /research_data/project1
```

### Step 4: Verify Changes

Re-check the permissions to confirm they have been applied correctly:
```bash
ls -l /research_data/project1
```

## Commands Summary

- `ls -l [path]`: List current permissions of the specified file or directory.
- `chmod [permissions] [path]`: Change the permissions of the specified file or directory.
- `chown [user] [path]`: Change the owner of the specified file or directory.
- `chgrp [group] [path]`: Change the group ownership of the specified file or directory.

## Example

1. Check current permissions:
   ```bash
   ls -l /research_data/project1
   ```

2. Set appropriate permissions:
   ```bash
   chmod 750 /research_data/project1
   ```

3. Verify the changes:
   ```bash
   ls -l /research_data/project1
   ```

## Conclusion

By following these steps, you can ensure that the research team has the appropriate file system permissions, maintaining the security and integrity of the data. This process involves examining existing permissions, determining the required authorization, and modifying permissions as necessary.

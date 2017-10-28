#### DNF Commands

This file is just a small documentation for all the dnf commands that may be needed

```bash
  # All repos are stored in the following folder /etc/yum.repos.d and to delete any
  # one of them, just go to that folder and delete the one that is not required.
  # This commands is used to display all the repos currently being used by dnf
  dnf repolist
  
  # To refresh the repolist call the previous command with --refresh flag
  dnf repolist --refresh
  
  # To view how many packages are installed
  dnf list --installed
  
  # dnf repo-pkgs <PACKAGE> list
```

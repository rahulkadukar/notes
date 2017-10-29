### Fedora installation

#### Setting up git

The following steps are used to generate the ssh key for easier github interaction.

```bash
  # Generate the SSH key
  ssh-keygen -t rsa -b 4096 -C "rahulkadukar@yahoo.com"

  # Add the private key using ssh-add
  ssh-add ~/.ssh/id_rsa

  # Now copy the public key and paste it into github
  cat ~/.ssh/id_rsa.pub
```

#### Enable SSH

This will enable remote login, so that this machine can be managed remotely

```bash
  # Install openssh-server if it is not installed. All actions done as root
  dnf install openssh-server

  # The following commands start and permanently enable the ssh daemon
  systemctl start sshd.service
  systemctl enable sshd.service
```

#### Configure vim and tmux

There is already a vim configuration file along with a sample theme and a tmux
configuration file that can be found in the following location

```bash
  https://github.com/rahulkadukar/notes/tree/master/config
```

Download from here and place into the correct location to enable a better vim
experience alongwith a few tmux tweaks. The following should be installed as well

```bash
  # All actions done as root
  dnf install tmux
  dnf install vim
  dnf install htop

  # Configuration of .bash_profile to enable tmux to start as tmux -2
  # Add the following line to your .bash_profile file
  alias tmux='tmux -2'
```

#### Install and configure vncserver

Download and install TigerVNC and allow it through the firewall

```bash
  # All actions done as root
  dnf install tigervnc-server

  # Allow it through the firewall
  firewall-cmd --add-service=vnc-server --permanent
  firewall-cmd --reload

  # Setup an initial password
  vncpasswd
```

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

# System Setup Project
ACIT2420
Name: Jaskirat Gill
Student ID: A01349758

This repository contains two projects for automating system setup and new user creation using Bash scripts.

## Project Structure

- `System-Setup-Scripts`: Contains scripts for system setup.
    - `system_setup_script`: Main script that calls the other setup scripts.
    - `install-packages`: Installs a list of packages specified in `package_names.txt`.
    - `create-symbolic-links`: Creates symbolic links for configuration files.
    - `package_names.txt`: File listing package names for installation (e.g., `kakoune`, `tmux`).

- `User-Creation-Script`: Contains the new user creation script.
    - `new-user-script`: Script to add a new user with options for custom shell, group memberships, and home directory setup.

## System Setup Scripts

Automates system setup by:
- Installing user-specified packages listed in `package_names.txt`.
- Creating symbolic links from configuration files stored in a Git repository to the appropriate system directories.

### Usage
1. Customize `package_names.txt` with required package names.
2. Run `system_setup_script` as root:
    ```bash
    sudo ./system_setup_script
    ```

## User Creation Script

- Automates new user creation by setting up:
    - A username and shell (default to /bin/bash).
    - A home directory with initial files copied from /etc/skel.
    - Optional group memberships.

### Usage

1. Run `new-user-script` as root with or without options.
    ```bash
    sudo ./new-user-script -u <username> -s <shell> -g <group1,group2,...>
    ```

    Running the script without options will create a default username with bash as the default shell.


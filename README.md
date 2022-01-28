# NAME
git-profile - manage local and global git configurations

# SYNOPSIS
**git-profile** \[OPTION ...] \[profile]

# DESCRIPTION
**git-profile** manages git configurations per work tree or globally. Running **git-profile** without arguments or options will display the current profile. Running **git-profile** with a single argument without options will switch the current profile to the first argument.

# SCOPE
**git-profile** can modify the local scope or the global scope. If the **--global** flag is not passed, the scope is assumed to be local. Global profiles follow git's normal rules for configuration, so local profiles inherit global properties unless they are overridden. If the local scope is used and the current working directory is not a git directory, then **git-profile** will exit.

# OPTIONS
**h**, **--help**
: displays a help menu

**-v**, **--version**
: displays the current version of git-profile

**--global**
: modify the global git configuration

**--local**
: modify the local git configuration

**-d**, **--dir**
: set the profile directory

**-l**, **--list**
: list available profiles

**-s**, **--save**
: save the current configuration as a profile with the name **profile**

**-r**, **--remove**
: remove a profile by name

# ENVIRONMENT

**$GIT_PROFILE_DIR**
: the default profile directory

# FILES

**git-profile** stores profiles and the current profile on the file system. The profile directory is selected using the following methods in order of priority: the **--dir** option, the **$GIT_PROFILE_DIR** variable, the directories listed below:

- **$XDG_CONFIG_DIR/git_profile/profiles**
- **$HOME/.config/git_profile/profiles**

# NOTES

Options that accept a value, which is currently only **--dir**, must be supplied a value in the form of **--option=value**. Values supplied in the subsequent argument are not supported at this time.

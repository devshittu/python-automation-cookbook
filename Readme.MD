# Chapter 1 Let's Begin Our Automation Journey
A convenient way of dealing with virtual environments, especially if you often have to swap between them, is to use the virtualenvwrapper module:

1. To install it, run this:
   > $ pip install virtualenvwrapper
2. Then, add the following variables to your shell startup script, these are normally .bashrc or .bash_profile. The virtual environments will be installed under the WORKON_HOME directory instead of the same directory as the project, as shown previously:

```bash
export WORKON_HOME="$HOME/.virtualenvs"
export VIRTUALENVWRAPPER_PYTHON="/usr/bin/python3"
export VIRTUALENVWRAPPER_VIRTUALENV="$HOME/.local/bin/virtualenv"

source /usr/local/bin/virtualenvwrapper.sh #for older linux
source ~/.local/bin/virtualenvwrapper.sh #for new linux

```

Sourcing the startup script or opening a new terminal will allow you to create new virtual environments:

> $ mkvirtualenv automation_cookbook
>
> Installing setuptools, pip, wheel...done.
> (automation_cookbook) $ deactivate
> $ workon automation_cookbook
> (automation_cookbook) $

List of available commands
lsvirtualenv
mkvirtualenv test
workon test
deactivate
rmvirtualenv test

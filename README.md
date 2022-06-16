# ansible-playbook-mac

An Ansible playbook for configuring a Mac :)

## Requirements (chicken and egg)

First, install dependencies that are required to run the playbook:

```bash
PYTHON_VERSION=3.10

# Install Command Line Tools (CLT) for Xcode
xcode-select --install

# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

# Install Python (includes pip3)
brew install python@${PYTHON_VERSION}

# Install Ansible
export PATH=/opt/homebrew/opt/python@${PYTHON_VERSION}/libexec/bin:${PATH}  # symlinks for generic python executables
export PATH=/opt/homebrew/opt/python@${PYTHON_VERSION}/bin:${PATH}  # symlinks for version-specific python executables
pip3 install --upgrade --user ansible
```

## Usage

Run the playbook to configure your Mac:

```bash
# Run Ansible playbook
export PATH=${HOME}/Library/Python/${PYTHON_VERSION}/bin:${PATH}  # user site pacakges for python
ansible-playbook -i "localhost," --ask-become-pass playbook.yml
```

## Credits

This playbook is a more minimal implementation of several other fantastic projects, including:

- [MacDevPlaybook](https://github.com/geerlingguy/mac-dev-playbook) (Jeff Geerling)
- [Strap](https://github.com/MikeMcQuaid/strap) (Mike McQuaid)
- [SuperLumic](https://github.com/superlumic/superlumic) (Roderik van der Veer)

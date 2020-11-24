# ansible-playbook-mac

An Ansible playbook for configuring my Mac

## Requirements (chicken and egg)

```bash
# Install Command Line Tools (CLT) for Xcode
xcode-select --install

# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

# Install Python 3.9
brew install python@3.9

# Install pip 3
curl -Lk https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py
/usr/local/bin/python3 /tmp/get-pip.py --user

# Install Ansible
export PATH=$HOME/Library/Python/3.9/bin:$PATH
/usr/local/bin/pip3 install --upgrade --user ansible
```

## Usage

```bash
# Run Ansible playbook
ansible-playbook -i "localhost," playbook.yml
```

# ansible-playbook-mac

An Ansible playbook for configuring my Mac

## Requirements (chicken and egg)

```
# Install pip
curl -Lk https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py
python /tmp/get-pip.py --user

# Install ansible
export PATH=$HOME/Library/Python/2.7/bin:$PATH
pip install --upgrade --user ansible
```

## Usage

```
ansible-playbook -i "localhost," playbook.yml
```

## ANSIBLE PULL
Using Ansible "Pull" Mode to Dynamically Automate Server/Workstation Builds.
### What is that?

- It comes with ansible - if you already have it installed, you have `ansible-pull`.
- Allows Servers/workstations to `pull` ansible playbooks from a Git server, and run them locally.

- No need to maintain a server, `no single point of failure`.
- Leverages the functionality of Git to extend Ansible.

### Ansible-Pull In Action

#### Step 1: Install Ansible on your Workstation

- Update package repo in your linux distro [debian or ubuntu]
```shell
sudo apt update

```
- Install Ansible
```shell
sudo apt install ansible
```
- Check Ansible Pull. You simply get ansible pull after installing ansible.
```shell
which ansible-pull
```
Expected result
```/usr/bin/ansible-pull```
#### Step 2: Setup a Git Repository
- Setup a git repository either private or public.
- Clone it into your workstation
- Change the working directory to that cloned folder

#### Step 2: Create Ansible playbook
- Inside the previously cloned repository
- Create an ansible playbook, use your favorite text editor. Ansible-pull expects a playbook named `local.yml`.


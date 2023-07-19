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
- Clone it into your workstation.
- Change the working directory to that cloned folder.

#### Step 3: Create Ansible playbook
- Inside the previously cloned repository.
- Create an ansible playbook, use your favorite text editor. Ansible-pull expects a playbook named `local.yml`.

- Add instructions to that file.
- Push changes into the Git remote repository `Github` or `Gitlab`.

#### Step 4: Install Ansible to all Target Servers.
- Update the packages repository for `Debian` or `Ubuntu` systems.
```shell
sudo apt update
```
- Install ansible 
```shell
sudo apt install ansible
```
- Again, verify ansible-pull
```shell
which ansible-pull
```

#### Step 5: Run Ansible-Pull to all Target Servers.
- Inside all target servers, run the Ansible pull command, to pull ansible playbooks from Github repo.
```shell
sudo ansible-pull -U https://github.com/samnzay/Ansible-Pull.git
```
>**Warning**: Remember to change your repository url accordingly.


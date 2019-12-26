# python
A python study repository. Test multiple ssh key.

## How do I add SSH public keys for the same machine to multiple GitHub accounts?

### Step One: Generate a new SSH key
```bash
sshkey -t rsa -b 4096 -C "your_email@host.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/your_name  //eg. Tom-php
// Test
ssh -T git@github.com
```

Add your public Key to Github.

### Step Two: setting config file
Create the config file in the path `~/.ssh/` and write some configuration information as below:

```bash
Host	Tomgit
HostName	github.com
User	git
IdentityFile ~/.ssh/Tom-php
```
### Step Three: change the origin url

```bash
git remote set-url origin Tomgit:your_github_username/your_repository.git
```


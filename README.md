# python
A python study repository. Test multiple ssh key.

```bash
sshkey -t rsa -b 4096 -C "your_email@host.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/your_name  //eg. Tom-php
// Test
ssh -T git@github.com
```

# bootstrap-git
Bootstrap git repository with some cool stuffs.
 - .gitignore for terraform and ansible-vault

## Keep your secret safe
First [install Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html) on your laptop.

After create ```.vault_pass``` file under the repository root folder and put in it a strong password.

Add in your .git/config file this code :
```
[diff "ansible-vault"]
  textconv = .git_crypt_diff
    # Do not cache the vault contents
	cachetextconv = false
[filter "ansible-vault"]
  clean  = .git_crypt_clean
```

**Please note : only work with the git cli !**

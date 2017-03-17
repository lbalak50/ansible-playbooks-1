## digital ocean play

Currently, it has `roles` for 

- `update` : update the apt-cache and upgrades it
- `bootstrap_server` : Installs some bare bones apt-packages and enables a minimal firewall
- `create_new_user`: Creates a new user called `tasdik` and copies the host's `.ssh/id_rsa` over to the new user's `.ssh` dir

#### Running it

```bash
$ ansible-playbook play.yml -vvv 
```
## digital ocean play

Currently, it has `roles` for 

- `update` : update the apt-cache and upgrades it
- `bootstrap_server` : Installs some bare bones apt-packages and enables a minimal firewall
- `create_new_user`: Creates a new user called `tasdik` and copies the host's `.ssh/id_rsa` over to the new user's `.ssh` dir
	- specify your hashed password inside the file `roles/create_new_user/defaults/main.yml`
	- generate your hashed password using 

```python
python -c 'import crypt; print crypt.crypt("<your-password>", "<your-key>")'
```

- `vimserver`: places the `.vimrc` server taken from my dotfiles and places it into the `~/.vimrc` for the user `tasdik`

#### Running it

```bash
$ ansible-playbook play.yml -vvv 
```
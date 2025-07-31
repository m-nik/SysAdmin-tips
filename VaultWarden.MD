

### Generate argon2 password for vaultwarden
```
sudo apt install argon2
echo -n "YourStrongAdminPassword" | argon2 "$(openssl rand -hex 16)" -id -t 2 -m 16 -p 1
```

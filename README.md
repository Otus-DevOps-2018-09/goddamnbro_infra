# goddamnbro_infra
goddamnbro Infra repository

-----------------

# SSH settings

Add to `~/.ssh/config`

```
Host bastion
  User godamnbro
  Hostname 35.204.23.214
  IdentityFile ~/.ssh/id_rsa_goddamnbro

Host someinternalhost
  User godamnbro
  Hostname 10.164.0.3
  Port 22
  IdentityFile ~/.ssh/id_rsa_goddamnbro
  ProxyCommand ssh -q -W %h:%p bastion
```

# VPN connection info

```
bastion_IP = 35.204.23.214
someinternalhost_IP = 10.164.0.3
```
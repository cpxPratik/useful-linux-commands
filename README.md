# useful-linux-commands

For running some of these commands, relevant package may need to be installed. It is recommended to run `man <command>` if details needed.

## Check firewalls

```sh
nmap <ip_address>
nmap -Pn <ip_address> # if ping is not allowed
```

## Check sha256 checksum

ref: <https://security.stackexchange.com/a/189004/199040>

```sh
sha256sum <filename>
```

## Check MD5 checksum

```sh
md5sum <filename>
```

## Empty a file

```sh
: > <filename>
or 
true > <filename>
or
echo > <filename>
```

## Shred a file

```sh
shred -vzu secrets.json
```

## List storage space usage

```sh
du -sh <directory>
du -sh projects/*
```

## See disk usage on linux and docker

```sh
lsblk
df -h
docker system df -v
docker ps -s
```

## Recover corrupt zsh history file

ref: <https://superuser.com/a/957924/412139>

```sh
mv .zsh_history .zsh_history_bad
strings .zsh_history_bad > .zsh_history
fc -R .zsh_history
```

## See available labels on nodes of docker swarm

ref: <https://stackoverflow.com/a/42419060/2137210>

```sh
docker node ls -q | xargs docker node inspect \
  -f '{{ .ID }} [{{ .Description.Hostname }}]: {{ range $k, $v := .Spec.Labels }}{{ $k }}={{ $v }} {{end}}'
```

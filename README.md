# useful-linux-commands

For running some of these commands, relevant package may need to be installed. It is recommended to run `man <command>` if details needed.

## To check firewalls

```sh
nmap <ip_address>
nmap -Pn <ip_address> # if ping is not allowed
```

## To check sha256 checksum

source: <https://security.stackexchange.com/a/189004/199040>

```sh
sha256sum <filename>_
```

## To check MD5 checksum

```sh
md5sum <filename>
```

## To empty a file

```sh
: > <filename>
or 
true > <filename>
or
echo > <filename>
```

## To shred a file

```sh
shred -vzu secrets.json
```

## List storage space usage

```sh
du -sh <directory>
du -sh projects/*
```

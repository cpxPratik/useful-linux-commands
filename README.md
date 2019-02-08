# useful-linux-commands

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

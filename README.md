# Webarchitects SSH Fingerprints

This repo contains SSH fingerprints for the following Webarchitects servers:

* [git.coop](https://git.coop/)
* [host2.webarch.net](https://host2.webarch.net/)
* [host3.webarch.net](https://host3.webarch.net/)
* [webarch1.co.uk](https://webarch1.co.uk/)
* [webarch2.co.uk](https://webarch2.co.uk/)
* [webarch3.co.uk](https://webarch3.co.uk/)
* [webarch4.co.uk](https://webarch4.co.uk/)
* [webarch5.co.uk](https://webarch5.co.uk/)
* [webarch6.co.uk](https://webarch6.co.uk/)
* [webarch7.co.uk](https://webarch7.co.uk/)

To install these fingerprints clone this repo into `~/.ssh`:

```bash
cd ~/.ssh
git clone https://git.coop/webarch/webarch-ssh.git
```

And then edit `~/.ssh/config` to add the following to the top of the file:

```
Include ~/.ssh/webarch-ssh/config
```

The server fingerprints and other SSH details can be found below in YAML format.

<!-- BEGIN 81.95.52.60 -->
## git.coop
SSH server configuration details for `git.coop` at `81.95.52.60`:
```yml
banner:
    comments: Debian-5+deb11u1
    protocol:
    - 2
    - 0
    raw: SSH-2.0-OpenSSH_8.4p1 Debian-5+deb11u1
    software: OpenSSH_8.4p1
compression:
- none
- zlib@openssh.com
enc:
- chacha20-poly1305@openssh.com
- aes256-gcm@openssh.com
- aes128-gcm@openssh.com
- aes256-ctr
- aes192-ctr
- aes128-ctr
fingerprints:
-   hash: 8nWVinsp5nSG9urdJoQEml4q8Kuu+VKILVGQghiv7Bg
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 4b:8a:35:8d:22:c0:33:fb:90:95:c6:db:74:32:4f:eb
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: SOtHe3ukCvoXvXopARa5bY4sPoARuJ3vCwXI/bGCoJ4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bd:ca:f8:e7:62:a4:ee:39:5c:56:8c:dd:26:6e:f3:f2
    hash_alg: MD5
    hostkey: ssh-rsa
kex:
-   algorithm: curve25519-sha256
-   algorithm: curve25519-sha256@libssh.org
-   algorithm: diffie-hellman-group18-sha512
-   algorithm: diffie-hellman-group16-sha512
-   algorithm: diffie-hellman-group14-sha256
-   algorithm: diffie-hellman-group-exchange-sha256
    keysize: 2048
key:
-   algorithm: ssh-ed25519
-   algorithm: rsa-sha2-512
    keysize: 2048
-   algorithm: rsa-sha2-256
    keysize: 2048
mac:
- hmac-sha2-512-etm@openssh.com
- hmac-sha2-256-etm@openssh.com
- umac-128-etm@openssh.com
target: localhost

```
The above YAML can generated using `ssh-keyscan -j 81.95.52.60 | yq -P`
<!-- END 81.95.52.60 -->

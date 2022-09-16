# Webarchitects SSH Fingerprints

This `git` repository contains [OpenSSH](https://www.openssh.com/) fingerprints for the following Webarchitects servers:

* [git.coop](#gitcoop)
* [host2.webarch.net](#host2webarchnet)
* [host3.webarch.net](#host3webarchnet)
* [webarch1.co.uk](#webarch1couk/)
* [webarch2.co.uk](#webarch2couk/)
* [webarch3.co.uk](#webarch3couk/)
* [webarch4.co.uk](#webarch4couk/)
* [webarch5.co.uk](#webarch5couk/)
* [webarch6.co.uk](#webarch6couk/)
* [webarch7.co.uk](#webarch7couk/)

See the [config](config) file for the list of hosts and the [known_hosts](known_hosts) file for the finferprints.

To install these fingerprints clone this repo into `~/.ssh`:

```bash
cd ~/.ssh
git clone https://git.coop/webarch/webarch-ssh.git
```

And then edit `~/.ssh/config` to add the following to the top of the file:

```
Include ~/.ssh/webarch-ssh/config
```

To update these fingerprints:

```bash
cd ~/.ssh/webarch-ssh
git pull
```

The contents of this repo have been automatically generated using the [Webarchitects SSH Ansible Role](https://git.coop/webarch/ssh), primary URL of this repo is [`https://git.coop/webarch/webarch-ssh`](https://git.coop/webarch/webarch-ssh) however it is also [mirrored to GitHub](https://github.com/webarch-coop/webarch-ssh).

The server fingerprints and other SSH details can be found below in YAML format.

<!-- BEGIN 81.95.52.60 -->
## git.coop
SSH server configuration details for `git.coop` at `81.95.52.60` generated on 2022-09-16 at 13:26:51:
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
<!-- BEGIN 81.95.52.6 -->
## host2.webarch.net
SSH server configuration details for `host2.webarch.net` at `81.95.52.6` generated on 2022-09-16 at 13:51:37:
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
-   hash: DAxdaqd2tSyueHikLkJlln2PWBDkJ5v7/PRtcSLblO0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: cf:4c:9a:13:84:e8:53:16:66:ae:cb:e0:b9:5f:c5:62
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: gmh/x49giAD2L+Fci/eFA0IJPbeKI6+qsw5OEOzGz+c
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 49:15:fb:f8:1e:0d:23:d6:95:61:04:5c:11:a4:2f:17
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.6 | yq -P`
<!-- END 81.95.52.6 -->
<!-- BEGIN 81.95.52.15 -->
## host3.webarch.net
SSH server configuration details for `host3.webarch.net` at `81.95.52.15` generated on 2022-09-16 at 13:53:07:
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
-   hash: XdP6rHAWWIUlFQ4EEUWqxlFyrNWRNCnZCznI9mlpxu8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 3c:12:c4:6c:10:90:bc:6a:c7:56:10:83:99:36:eb:c1
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: bnsZNSIFYSFdWJIfP8r8MUiJSgyFdV+mRX0UAsupdnA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 1d:9a:6f:74:54:b3:f4:16:c2:e8:54:1c:f3:a8:65:6d
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.15 | yq -P`
<!-- END 81.95.52.15 -->
<!-- BEGIN 81.95.52.61 -->
## webarch1.co.uk
SSH server configuration details for `webarch1.co.uk` at `81.95.52.61` generated on 2022-09-16 at 12:54:14:
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
-   hash: YS5euQzn+tskGwhoUMJjonKoq6cUIt09ofDBayfhnts
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: bb:a2:5a:c2:c5:7e:ac:1f:24:23:9d:86:0b:50:15:e7
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: QI1ALRSfqNirgnrvhA1oI2xMPzKv6SIxpX9QMESivBo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 26:c5:67:f7:5e:08:80:53:d4:04:f7:d9:53:ef:21:94
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.61 | yq -P`
<!-- END 81.95.52.61 -->
<!-- BEGIN 81.95.52.62 -->
## webarch2.co.uk
SSH server configuration details for `webarch2.co.uk` at `81.95.52.62` generated on 2022-09-16 at 12:51:43:
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
-   hash: PnsDhdiXkrSvew6o10/bdEtteKmF340t9YfIXrnIL3s
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 49:69:e5:62:b5:33:6a:49:fc:80:5a:3b:a4:77:d0:3f
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: mtIdVhfRNjzjhpsXbSyzjhi3GHAqPJQuVcoBSRMxXuI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 78:31:45:45:d8:b2:8f:ae:7b:74:3f:fa:3d:88:18:b2
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.62 | yq -P`
<!-- END 81.95.52.62 -->
<!-- BEGIN 81.95.52.63 -->
## webarch3.co.uk
SSH server configuration details for `webarch3.co.uk` at `81.95.52.63` generated on 2022-09-16 at 12:53:07:
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
-   hash: 8hVVrS25qQsp2WNQi7iUC0HaFzmGbvpJdCd1tTznfaw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 64:3c:6e:01:2b:fe:f9:48:ec:92:f3:87:4b:85:43:51
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: BmHGwHiwInhuKq4xbVNbJg+fRv2wVZWyvzUwvw+C8AI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 84:da:0b:27:96:33:ad:a3:2c:47:68:92:f7:c6:e6:70
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.63 | yq -P`
<!-- END 81.95.52.63 -->
<!-- BEGIN 81.95.52.64 -->
## webarch4.co.uk
SSH server configuration details for `webarch4.co.uk` at `81.95.52.64` generated on 2022-09-16 at 12:50:29:
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
-   hash: X4QnGRi8EEzUzewwqONvK4M97cuFPn0mvR3NL8WftII
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 76:55:e0:dd:dc:69:6a:60:da:62:5a:9a:dc:2f:d4:6c
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ETFAIJf543GyTNO3IwWSh4Lh3j2XessMtlX0/b30yl0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 25:ab:9c:23:a0:b5:b4:10:36:9d:04:93:dd:4f:41:1b
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.64 | yq -P`
<!-- END 81.95.52.64 -->
<!-- BEGIN 81.95.52.65 -->
## webarch5.co.uk
SSH server configuration details for `webarch5.co.uk` at `81.95.52.65` generated on 2022-09-16 at 12:51:44:
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
-   hash: iJo+CkR5cpbpJYkKAaZGJdtZdgywAeegoc82ZCDxGcQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: d3:87:f2:5b:05:5b:8b:e2:d0:b2:4b:18:b0:a9:11:d0
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 134bSuKj2+9qhsQct1i1ge37u19kKY8z5BetytTYTiY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ac:cc:8e:56:1c:c8:04:fd:6d:c3:16:8b:bf:f2:ec:60
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.65 | yq -P`
<!-- END 81.95.52.65 -->
<!-- BEGIN 81.95.52.76 -->
## webarch6.co.uk
SSH server configuration details for `webarch6.co.uk` at `81.95.52.76` generated on 2022-09-16 at 12:58:40:
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
-   hash: maTEv1v0Md56HdVTzInPeZ7PleCA46vf5vuOGFBEFDg
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 58:4e:72:d4:54:c1:0a:9e:54:18:e1:96:75:f9:bd:c9
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 8bbn+uWpYMxuW9EvP8Rb8nWpZxjDRIUp4ZEpIBeHyUU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 96:43:45:0d:19:3d:cc:e7:77:26:a9:98:a3:a2:dc:f7
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.76 | yq -P`
<!-- END 81.95.52.76 -->
<!-- BEGIN 81.95.52.67 -->
## webarch7.co.uk
SSH server configuration details for `webarch7.co.uk` at `81.95.52.67` generated on 2022-09-16 at 12:54:16:
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
-   hash: dv2BBi8g+G0mYPCSz7NDaoVCwwX/OZGRsx0oA2il/tI
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 9e:4b:0e:92:e2:a3:19:00:ad:02:db:37:b1:fd:f5:67
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: kFUrvamfWtXBVv8ZOkB4yWeDrevxNTMGAi4uElBMmKg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 13:15:12:42:c1:46:1d:55:43:5b:5b:12:84:dc:b7:bb
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
The above YAML can generated using `ssh-keyscan -j 81.95.52.67 | yq -P`
<!-- END 81.95.52.67 -->

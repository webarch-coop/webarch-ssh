# Webarchitects SSH Fingerprints

This `git` repository contains [OpenSSH](https://www.openssh.com/) fingerprints for the following Webarchitects git and shared hosting servers:

* [git.coop](#gitcoop)
* [host2.webarch.net](#host2webarchnet)
* [host3.webarch.net](#host3webarchnet)
* [webarch1.co.uk](#webarch1couk)
* [webarch2.co.uk](#webarch2couk)
* [webarch3.co.uk](#webarch3couk)
* [webarch4.co.uk](#webarch4couk)
* [webarch5.co.uk](#webarch5couk)
* [webarch6.co.uk](#webarch6couk)
* [webarch7.co.uk](#webarch7couk)

See the [config](config) file for the list of hosts and the [known_hosts](known_hosts) file for the fingerprints.

You can download these SSH fingerprints as [a zip file](https://git.coop/webarch/webarch-ssh/-/archive/1.0.0/webarch-ssh-1.0.0.zip) (other [formats available](https://git.coop/webarch/webarch-ssh/-/releases/1.0.0)) and uncompress the archive into `~/.ssh/webarch-ssh`.

And then edit `~/.ssh/config` to add the following to the top of the file:

```
Include ~/.ssh/webarch-ssh/config
```

Or install these fingerprints using `git`, clone this repo into `~/.ssh`:

```bash
cd ~/.ssh
git clone https://git.coop/webarch/webarch-ssh.git
```

And update these fingerprints using `git`:

```bash
cd ~/.ssh/webarch-ssh
git pull
```

The contents of this repo have been automatically generated using the [Webarchitects SSH Ansible Role](https://git.coop/webarch/ssh), primary URL of this repo is [`https://git.coop/webarch/webarch-ssh`](https://git.coop/webarch/webarch-ssh) however it is also [mirrored to GitHub](https://github.com/webarch-coop/webarch-ssh).

The server fingerprints and other SSH details can be found below in YAML format, `yq` is [available from GitHub](https://github.com/mikefarah/yq), we have written [a yq Ansible role](https://git.coop/webarch/yq) to install it.

<!-- BEGIN 81.95.52.60 -->
## git.coop
SSH server fingerprints for `git.coop` at `81.95.52.60`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.60 | jq .fingerprints | yq -P`
<!-- END 81.95.52.60 -->
<!-- BEGIN 81.95.52.6 -->
## host2.webarch.net
SSH server fingerprints for `host2.webarch.net` at `81.95.52.6`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.6 | jq .fingerprints | yq -P`
<!-- END 81.95.52.6 -->
<!-- BEGIN 81.95.52.15 -->
## host3.webarch.net
SSH server fingerprints for `host3.webarch.net` at `81.95.52.15`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.15 | jq .fingerprints | yq -P`
<!-- END 81.95.52.15 -->
<!-- BEGIN 81.95.52.61 -->
## webarch1.co.uk
SSH server fingerprints for `webarch1.co.uk` at `81.95.52.61`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.61 | jq .fingerprints | yq -P`
<!-- END 81.95.52.61 -->
<!-- BEGIN 81.95.52.62 -->
## webarch2.co.uk
SSH server fingerprints for `webarch2.co.uk` at `81.95.52.62`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.62 | jq .fingerprints | yq -P`
<!-- END 81.95.52.62 -->
<!-- BEGIN 81.95.52.63 -->
## webarch3.co.uk
SSH server fingerprints for `webarch3.co.uk` at `81.95.52.63`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.63 | jq .fingerprints | yq -P`
<!-- END 81.95.52.63 -->
<!-- BEGIN 81.95.52.64 -->
## webarch4.co.uk
SSH server fingerprints for `webarch4.co.uk` at `81.95.52.64`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.64 | jq .fingerprints | yq -P`
<!-- END 81.95.52.64 -->
<!-- BEGIN 81.95.52.65 -->
## webarch5.co.uk
SSH server fingerprints for `webarch5.co.uk` at `81.95.52.65`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.65 | jq .fingerprints | yq -P`
<!-- END 81.95.52.65 -->
<!-- BEGIN 81.95.52.76 -->
## webarch6.co.uk
SSH server fingerprints for `webarch6.co.uk` at `81.95.52.76`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.76 | jq .fingerprints | yq -P`
<!-- END 81.95.52.76 -->
<!-- BEGIN 81.95.52.67 -->
## webarch7.co.uk
SSH server fingerprints for `webarch7.co.uk` at `81.95.52.67`:
```yml
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

```
The above YAML can generated using `ssh-audit -j 81.95.52.67 | jq .fingerprints | yq -P`
<!-- END 81.95.52.67 -->

# DNS servers

* [dns0.webarchitects.co.uk](#dns0webarchitectscouk)
* [dns1.webarchitects.co.uk](#dns1webarchitectscouk)
* [dns2.webarch.info](#dns2webarchinfo)
* [dns3.webarch.info](#dns3webarchinfo)
* [dns4.webarch.info](#dns4webarchinfo)
* [dns5.webarchitects.co.uk](#dns5webarchitectscouk)

<!-- BEGIN 81.95.52.24 -->
## dns0.webarchitects.co.uk
SSH server fingerprints for `dns0.webarchitects.co.uk` at `81.95.52.24`:
```yml
-   hash: U66Vm8vkhWcHUiFjaxSgBWOw7daZCFYJMjoP8mR/tuo
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 65:c4:71:91:3f:e3:4b:87:3b:15:19:a1:c0:6c:da:6a
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: wjugQ3TZ6kjP0cO46DNM1zkVkExn3/wrr0WgM4yWTnY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c5:37:0f:04:8e:21:cc:b8:b8:bb:3e:f4:f0:e3:f9:2f
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.24 | jq .fingerprints | yq -P`
<!-- END 81.95.52.24 -->
<!-- BEGIN 81.95.52.30 -->
## dns1.webarchitects.co.uk
SSH server fingerprints for `dns1.webarchitects.co.uk` at `81.95.52.30`:
```yml
-   hash: mT9iSmiQ+UTa47nGKK+o03fjY8O/XPn0innIQODu1G4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: f7:31:82:2c:24:f7:94:5c:b2:fa:06:91:8c:09:36:2e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: G7XBpl/Xtp5tiMVZQSbTDcdrd4DU2w1hafq1GQ5oPH8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 4c:e9:3d:d8:5b:7f:ab:55:a0:54:24:17:df:06:5a:84
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.30 | jq .fingerprints | yq -P`
<!-- END 81.95.52.30 -->
<!-- BEGIN 217.70.190.127 -->
## dns2.webarch.info
SSH server fingerprints for `dns2.webarch.info` at `217.70.190.127`:
```yml
-   hash: zmb781UaQbVjM1IBYbrDyaFdUMC8GrbgQwGuhyKKHig
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 96:31:60:99:51:39:b8:23:8a:45:e2:8f:ec:2d:e0:10
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: YpCLxqckDBzM09l2R6Y03qPSfL6xrDi2GEJ4YPKLY2U
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 46:8b:da:9d:80:b5:93:30:98:12:0c:df:9d:61:70:45
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 217.70.190.127 | jq .fingerprints | yq -P`
<!-- END 217.70.190.127 -->
<!-- BEGIN 185.112.146.79 -->
## dns3.webarch.info
SSH server fingerprints for `dns3.webarch.info` at `185.112.146.79`:
```yml
-   hash: VfHfL1lX6MyEvxzKVpFNxQlgmDMY1NQeDJLSTlteKbw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 93:36:e8:cc:c4:13:8d:b4:0c:24:47:67:c4:2d:67:bd
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: tegfguzTkXdIIePQ9xGyNxEP0DzjYxU1UCXkWKigUiI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5b:82:82:6d:97:4b:94:0a:a7:9c:6f:ce:cf:7c:01:c2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 185.112.146.79 | jq .fingerprints | yq -P`
<!-- END 185.112.146.79 -->
<!-- BEGIN 23.237.136.75 -->
## dns4.webarch.info
SSH server fingerprints for `dns4.webarch.info` at `23.237.136.75`:
```yml
-   hash: ZYLyCtj3NtE/aLzGYC3wXNnJG4phB6ZksI+yyfD0Wk0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 15:e8:f8:ea:1d:38:fb:b2:73:9b:5f:ac:a3:43:00:79
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: xppdf6iTkZto2gWef90Nyw4wxIiMtFnd9zyd8iq5aMo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f9:8a:e1:74:c2:1f:86:fa:41:ec:34:cd:6c:dd:c2:d2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 23.237.136.75 | jq .fingerprints | yq -P`
<!-- END 23.237.136.75 -->
<!-- BEGIN 81.95.52.27 -->
## dns5.webarchitects.co.uk
SSH server fingerprints for `dns5.webarchitects.co.uk` at `81.95.52.27`:
```yml
-   hash: oLlyMFwnHqeGHXZVBx6XAU5yDJX/ddD2nImg490MKy8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: fc:5d:86:51:89:33:68:bd:f9:f7:84:f1:e2:66:7f:a2
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: NVCNPZU+QblTtYIEWneunlpmjXZ5DAoWxwa2XHoy9uo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 9b:16:cb:f1:17:b2:6e:88:cd:de:1e:ac:9d:66:f2:61
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.27 | jq .fingerprints | yq -P`
<!-- END 81.95.52.27 -->

# Development servers

* [discourse.webarchitects.org.uk](#discoursewebarchitectsorguk)
* [icinga-master.webarchitects.org.uk](#icinga-masterwebarchitectsorguk)
* [nextcloud.webarch.org.uk](#nextcloudwebarchorguk)
* [onlyoffice.webarchitects.org.uk](#onlyofficewebarchitectsorguk)
* [wsh.webarchitects.org.uk](#wshwebarchitectsorguk)

<!-- BEGIN 81.95.52.92 -->
## discourse.webarchitects.org.uk
SSH server fingerprints for `discourse.webarchitects.org.uk` at `81.95.52.92`:
```yml
-   hash: 4G44F377gR/26bQthk7DdCZCxOHNpe7Q+8s2mlzr1PU
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 66:48:42:dd:36:24:86:ac:fa:78:ef:73:bf:34:91:9e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: jgRbl+SULj7cLnx9usmQrRKUz3AGco+G6isB40wYpNU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bd:06:59:4d:47:38:a9:28:9c:f5:22:d3:06:08:f2:2b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.92 | jq .fingerprints | yq -P`
<!-- END 81.95.52.92 -->
<!-- BEGIN 81.95.52.42 -->
## icinga-master.webarchitects.org.uk
SSH server fingerprints for `icinga-master.webarchitects.org.uk` at `81.95.52.42`:
```yml
-   hash: DmZbbmxocn8jZmR/jsXxJw80Yu13f9YkB381nLKjXcY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: cd:a7:ba:2e:66:19:4f:43:37:38:ad:67:64:bf:2f:fc
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: HrfrLIdnON6j/MsgYZstNro525IjNnHffBf5Kqgmbnw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 3e:39:5a:fe:cc:c8:cc:ba:a8:2e:56:40:49:a5:a6:c6
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.42 | jq .fingerprints | yq -P`
<!-- END 81.95.52.42 -->
<!-- BEGIN 81.95.52.26 -->
## nextcloud.webarch.org.uk
SSH server fingerprints for `nextcloud.webarch.org.uk` at `81.95.52.26`:
```yml
-   hash: oAiCmiXulH7u0S7hCMOQSyLi4W0r7XrCQyjJSKp/FR0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 5c:41:0e:5b:a9:52:a6:2c:54:0c:a2:a2:16:0d:0e:07
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 03mD18qPttZ+q4Og97FuJTXG8T36SSOye8CkM8cF1zo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ac:49:0e:ee:11:fd:91:3b:f1:2c:0c:c1:15:e1:ff:a4
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.26 | jq .fingerprints | yq -P`
<!-- END 81.95.52.26 -->
<!-- BEGIN 81.95.52.88 -->
## onlyoffice.webarchitects.org.uk
SSH server fingerprints for `onlyoffice.webarchitects.org.uk` at `81.95.52.88`:
```yml
-   hash: kE+2Q9GoP0gfatKYZmEE1wQqk2ogKDiO8KFU25rLAOY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 9a:3a:ed:62:a8:73:86:4d:78:9b:e1:6b:28:5c:62:85
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: nCejHYIwnPbE97OqT8uMGX0i5UzxlHQJ60Uw2kg2I7g
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c5:1c:8d:ab:f9:97:08:78:13:7e:76:24:41:69:ee:db
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.88 | jq .fingerprints | yq -P`
<!-- END 81.95.52.88 -->
<!-- BEGIN 81.95.52.56 -->
## wsh.webarchitects.org.uk
SSH server fingerprints for `wsh.webarchitects.org.uk` at `81.95.52.56`:
```yml
-   hash: HgnaipZfbe+JWZkr/jjt72Y0y7hGI4kcK1M1qyYDoHY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: df:b2:66:6d:56:89:88:5e:ff:44:89:ab:e0:1e:85:d2
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: Y2tCvB+YxBLCA5xyeXGiHH5OzW2wSRcUqRpzzjYT7Z0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f0:bd:d4:7b:bc:9c:33:a0:bf:8e:cb:2f:7b:26:bf:e4
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.56 | jq .fingerprints | yq -P`
<!-- END 81.95.52.56 -->

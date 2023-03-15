# Webarchitects SSH Fingerprints

This `git` repository contains [OpenSSH](https://www.openssh.com/) fingerprints for the following Webarchitects git and shared hosting servers (and many other additional servers that have only a small number of users):

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

Please use the fingerprints below to verify your SSH connection when you first connect to our servers.

## OpenSSH users

If you use [OpenSSH](https://www.openssh.com/) then you can install these fingerprints locally, the best way to do this is using `git` as this will result in the most recent version of this repository and it will make it easier to update the configuration.

The following instructions assume you are running Linux or something like it and your shell is Bash, or something like it.

Open a terninal client and check that you have OpenSSH, run

```bash
ssh -V
```

It should output the version of OpenSSH that you ahve installed:

```
OpenSSH_9.2p1 Debian-2, OpenSSL 3.0.8 7 Feb 2023]
```

Check that you have `git`, run:

```bash
git -v
```

It should output the version of `git` that you ahve installed:

```
git version 2.39.2
```

Then change into your `~/.ssh` directory, the following command will create the directory if it doesn't exist and then change into it (the tilda character, `~` is a shortcut for your `$HOME` directory):

```bash
cd ~/.ssh || mkdir ~/.ssh ; chmod 0700 ~/.ssh ; cd ~/.ssh
```

Check that you are in the the `~/.ssh` directory:

```bash
pwd
```

Then clone this repo:

```bash
git clone https://git.coop/webarch/webarch-ssh.git
```

And then either manually add the follwing line to to the top of your `~/.ssh/config` file:

```
Include ~/.ssh/webarch-ssh/config
```

Or run this command for the file to be created with this content or the content to be appended to an existing file:

```bash
echo "Include ~/.ssh/webarch-ssh/config" >> ~/.ssh/config
```

And then when you need to update the fingerprints run:

```bash
cd ~/.ssh/webarch-ssh
git pull
```

If you can't use `git` you can download the SSH configuration as [a zip file](https://git.coop/webarch/webarch-ssh/-/archive/1.2.0/webarch-ssh-1.2.0.zip) (other [formats available](https://git.coop/webarch/webarch-ssh/-/releases/1.2.0)) and uncompress the archive into `~/.ssh/webarch-ssh`.

And then edit `~/.ssh/config` to add the following to the top of the file:

```
Include ~/.ssh/webarch-ssh/config
```

*However* please note that updating is harder when not using `git` and in addition we update the repo when we add and remove servers but don't always generate a release when this is done so the archive files might well be out of date.

## Fingerprints repo

The contents of this repo have been automatically generated using the [Webarchitects SSH Ansible Role](https://git.coop/webarch/ssh), primary URL of this repo is [`https://git.coop/webarch/webarch-ssh`](https://git.coop/webarch/webarch-ssh) however it is also [mirrored to GitHub](https://github.com/webarch-coop/webarch-ssh).

See the [config](config) file for the list of hosts and the [known_hosts](known_hosts) file for the fingerprints.

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

# Monitoring servers

* [icinga.webarch.net](#icingawebarchnet)
* [monitor.webarch.net](#monitorwebarchnet)

<!-- BEGIN 93.95.228.246 -->
## icinga.webarch.net
SSH server fingerprints for `icinga.webarch.net` at `93.95.228.246`:
```yml
-   hash: Pzo2yBBx8FY0z/QEHvQN0PMrP/Vrmzys7I4n0pDWcxw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 3d:aa:d5:0d:32:35:19:f5:c9:dc:b6:4c:76:f8:82:a0
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: rCVkGSn1NEheh7U2J4QNveQ6TMr8uins95ogpRGCaTI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 59:43:a8:09:c0:eb:11:59:bc:9a:55:5f:ec:ec:f2:31
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 93.95.228.246 | jq .fingerprints | yq -P`
<!-- END 93.95.228.246 -->
<!-- BEGIN 81.95.52.37 -->
## monitor.webarch.net
SSH server fingerprints for `monitor.webarch.net` at `81.95.52.37`:
```yml
-   hash: 6xDbxi8+aJUgNipOOyoyIF1ZTWsoP1KPI9hxVf1Oy6w
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: ee:09:97:99:53:a2:a2:b5:53:30:c2:b7:a0:82:4f:54
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: HJP3OeWVTmm2gGmL9E0wayMs+181ie0u0uS/+td3rGQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: a8:d8:4e:5f:fe:8a:ce:a0:22:cd:aa:c8:68:e3:e8:b8
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.37 | jq .fingerprints | yq -P`
<!-- END 81.95.52.37 -->

# ONLYOFFICE servers

* [onlyoffice1.webarch.net](#onlyoffice1webarchnet)
* [onlyoffice2.webarch.net](#onlyoffice2webarchnet)

<!-- BEGIN 81.95.52.87 -->
## onlyoffice1.webarch.net
SSH server fingerprints for `onlyoffice1.webarch.net` at `81.95.52.87`:
```yml
-   hash: Y8cQsxuQ5EHkY5MPChMB1k7ubjxAtGraeEGlMFpLH9Y
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b5:28:4c:1a:95:4c:50:c3:f4:57:49:cb:c1:1b:10:70
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 2umCQHgQZcAq+0obQkaixDw1qvdMHZnUnOE1BiGmlVo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f0:43:61:98:f2:57:11:e4:c1:89:6a:93:54:36:08:0d
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.87 | jq .fingerprints | yq -P`
<!-- END 81.95.52.87 -->
<!-- BEGIN 81.95.52.90 -->
## onlyoffice2.webarch.net
SSH server fingerprints for `onlyoffice2.webarch.net` at `81.95.52.90`:
```yml
-   hash: tUaFhdJKv5hj58tSb0xf+pim8aOzz5A6lBg2GfviXLo
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 9b:ae:a2:d3:bb:3a:1e:8a:cc:be:31:af:53:72:18:d6
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: Smg6QrunBrS9DqX0hkEYwidnJcMIq/G6pvTZMaCbB7g
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f4:1b:6e:aa:cb:b7:24:36:f0:c0:8c:f9:a7:91:e5:cd
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.90 | jq .fingerprints | yq -P`
<!-- END 81.95.52.90 -->

# Discourse servers

* [cotechforum.webarch.net](#cotechforumwebarchnet)
* [workersforum.webarch.coop](#workersforumwebarchcoop)
* [members.webarchitects.coop](#memberswebarchitectscoop)
* [forum.meet.coop](#forummeetcoop)
* [radhr.webarch.net](#radhrwebarchnet)

<!-- BEGIN 81.95.52.58 -->
## forum.cotech.uk
SSH server fingerprints for `forum.cotech.uk` at `81.95.52.58`:
```yml
-   hash: VGWa72gsx0iMLa+HDynGOnqyOJ/OSloosGOUZGG4QgM
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 0b:91:31:e2:50:7e:20:9d:d3:38:5c:69:0d:c8:c3:6b
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: cIfhk58Yt1bbAEILZ4Z1/0TzM39fHIukMmqlps3/xfI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: be:ba:3a:77:c3:4f:de:dc:77:4c:fb:97:44:07:b7:22
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.58 | jq .fingerprints | yq -P`
<!-- END 81.95.52.58 -->
<!-- BEGIN 81.95.52.12 -->
## forum.workers.coop
SSH server fingerprints for `forum.workers.coop` at `81.95.52.12`:
```yml
-   hash: CZO1LP4fmImb049C5xfFkuqrRDn2/9+YFwT6tfTVkzo
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 15:be:d4:af:94:4d:10:ad:f6:6a:3d:37:de:10:52:d6
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: I+BW1QegYbchKNkrk+waGTk8/CrZ0o9R0pCu4OK9fsg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: db:dc:ee:55:8c:57:83:47:87:88:01:98:45:94:9a:b3
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.12 | jq .fingerprints | yq -P`
<!-- END 81.95.52.12 -->
<!-- BEGIN 81.95.52.93 -->
## members.webarchitects.coop
SSH server fingerprints for `members.webarchitects.coop` at `81.95.52.93`:
```yml
-   hash: AArx85YXV8jN+5S+Yk0R93m31ycCHY8WRhnkbX137g0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 9e:26:2d:bc:8c:18:09:e2:b8:44:6b:f7:b3:c0:e5:0a
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 9pednZ+rr3ic3fmKVpYdx95T3kDGB4ibP4/gwgApgDg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 16:9c:f1:48:7d:d5:bb:12:51:a1:01:d8:e5:84:e2:aa
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.93 | jq .fingerprints | yq -P`
<!-- END 81.95.52.93 -->
<!-- BEGIN 81.95.52.40 -->
## forum.meet.coop
SSH server fingerprints for `forum.meet.coop` at `81.95.52.40`:
```yml
-   hash: /cg9jjtL2U+ehFjxVa4MSdZTkv8VBei6Kjney3xf0Ss
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 67:6f:43:0b:33:09:96:41:57:6b:28:88:74:51:70:48
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: UcI0ygXhCfV25PaJgamuQyrbGZXZ95glu5mSLYvYXSQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 50:10:96:a7:e6:a1:89:92:8b:31:bd:c4:d5:56:39:f8
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.40 | jq .fingerprints | yq -P`
<!-- END 81.95.52.40 -->
<!-- BEGIN 81.95.52.33 -->
## radhr.webarch.net
SSH server fingerprints for `radhr.webarch.net` at `81.95.52.33`:
```yml
-   hash: yrXOnykC7x1lBd7+ZNR4m+n2VYnfIjngsWPNtBFM2DQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 70:3d:eb:20:26:8f:1e:cd:04:d6:05:4c:56:b7:29:7c
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: DCYHBqgVHabzdo/AVUbtZxA3gTjPGU5HM+XMnfnINpk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 89:69:ff:d6:28:35:b7:cd:2c:8c:97:b5:50:fe:c9:bf
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.33 | jq .fingerprints | yq -P`
<!-- END 81.95.52.33 -->

# Web servers

* [office.webarchitects.co.uk](#officewebarchitectscouk)
* [web.webarch.net](#webwebarchnet)
* [ods.webarch.net](#odswebarchnet)
* [3dccloud.webarch.net](#3dccloudwebarchnet)
* [ldn.webarch.net](#ldnwebarchnet)
* [cloud.assist.coop](#cloudassistcoop)
* [cloud.inca.coop](#cloudincacoop)
* [office.energytransitions.uk](#officeenergytransitionsuk)
* [sanford.webarch.net](#sanfordwebarchnet)
* [office.unitedigitaltech.org](#officeunitedigitaltechorg)
* [cloud.leedsbread.coop](#cloudleedsbreadcoop)
* [imc.indymedia.org.uk](#imc.indymedia.org.uk)
* [oriole.webarch.net](#oriolewebarchnet)
* [animorph.webarch.coop](#animorphwebarchcoop)
* [sharedfutures.webarch.net](#sharedfutureswebarchnet)
* [greenham.webarch.net](#greenhamwebarchnet)
* [sharenergy.webarch.net](#sharenergywebarchnet)
* [holyoake.webarch.coop](#holyoakewebarchcoop)
* [web.cotech.uk](#webcotechuk)
* [redirect.webarch.net](#redirectwebarchnet)
* [j25.webarch.net](#j25webarchnet)
* [cloud.croome.net](#cloudcroomenet)

<!-- BEGIN 81.95.52.100 -->
## office.webarchitects.co.uk
SSH server fingerprints for `office.webarchitects.co.uk` at `81.95.52.100`:
```yml
-   hash: sS08QjKBtnwzWv8MvVt8LzvCToe2tpMCzWSR3jCfjuA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 7b:77:74:28:2b:ef:ca:41:70:08:b5:92:d1:b6:cf:a6
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ZfJPTwthoFHdBTYjcPTRmnWne4YlntgaUiUIyrD/vgg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d3:35:bf:c4:50:dd:02:18:9d:20:1d:a0:01:c3:04:20
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.100 | jq .fingerprints | yq -P`
<!-- END 81.95.52.100 -->
<!-- BEGIN 81.95.52.98 -->
## web.webarch.net
SSH server fingerprints for `web.webarch.net` at `81.95.52.98`:
```yml
-   hash: YBHyTapTl/1lwURysWfJZmm8ovnjixgDpsIBEwNzkh8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 56:6c:f9:dd:74:18:a2:f1:51:20:41:7b:ec:54:c3:6e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: CCam2VrRo0WC30o/y9oSYRSDMhcSqjEJgBckURdtz/k
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 1e:c4:30:31:31:84:53:6b:48:ff:47:00:8c:ed:e9:99
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.98 | jq .fingerprints | yq -P`
<!-- END 81.95.52.98 -->
<!-- BEGIN 81.95.52.14 -->
## ods.webarch.net
SSH server fingerprints for `ods.webarch.net` at `81.95.52.14`:
```yml
-   hash: KwBIARUoND3Np5BkLojKmE2s+y47xtxZ60zCGfxow8M
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c0:65:76:0d:95:ae:02:81:05:b6:bd:b9:b9:8d:f1:d4
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: yIjhGADpzvQZthEQQpTVMvEtzl4kFNCIDzRav9yz8qQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d4:d3:ec:9d:dd:18:95:ce:fe:df:8d:f7:86:c4:c2:f1
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.14 | jq .fingerprints | yq -P`
<!-- END 81.95.52.14 -->
<!-- BEGIN 81.95.52.55 -->
## 3dccloud.webarch.net
SSH server fingerprints for `3dccloud.webarch.net` at `81.95.52.55`:
```yml
-   hash: hapOsjA3THlfM4EY4ZW3golYY1mNOu6u0ntV9J5EC3Y
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c1:9e:e6:68:96:91:22:4f:52:da:5b:bf:9c:fe:56:49
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: tOJEGYqT2JnaQDkDC4pkEiRpvTLD52UCloI8l1GS89Q
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0f:76:76:b9:60:cb:a2:bb:f4:ce:d1:92:5d:50:c3:b5
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.55 | jq .fingerprints | yq -P`
<!-- END 81.95.52.55 -->
<!-- BEGIN 81.95.52.43 -->
## ldn.webarch.net
SSH server fingerprints for `ldn.webarch.net` at `81.95.52.43`:
```yml
-   hash: TRfk4nwz8fhG46gSely9rQCE8FahXl6bQwuVkMhp7f8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 42:0e:68:13:7c:58:ce:05:a7:6c:88:8b:e2:b7:f6:9f
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: KkskTszgnOFDJWeBFw/IwXEMii8k96Z0sYMvzarXMfw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ed:e4:46:c6:5b:0a:69:f8:a4:39:55:63:de:f7:10:11
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.43 | jq .fingerprints | yq -P`
<!-- END 81.95.52.43 -->
<!-- BEGIN 81.95.52.103 -->
## cloud.assist.coop
SSH server fingerprints for `cloud.assist.coop` at `81.95.52.103`:
```yml
-   hash: MsRG6Ie4vfjelw7HqpMHh7F4SW25sVGIshJLVO++D78
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 6d:b4:73:01:78:bf:94:2b:e3:d7:5c:26:3c:ec:f5:7d
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: QKE19oyp/juru2GXKMXeGcRYoNm902NmR2bR8NpU6eU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 11:1e:2b:9e:f4:fa:55:7f:20:07:72:c1:0d:58:64:d5
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.103 | jq .fingerprints | yq -P`
<!-- END 81.95.52.103 -->
<!-- BEGIN 81.95.52.31 -->
## cloud.inca.coop
SSH server fingerprints for `cloud.inca.coop` at `81.95.52.31`:
```yml
-   hash: A2NFSx8W7dZM22mAV0KxnMexh9BoLR/8lHV+0/fH2HM
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 59:b0:75:f2:55:8e:fa:be:cd:99:2a:1b:74:ec:d8:be
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ksvKEFRpvLzeAz87f2Ms3zr3v4URk1pkIwE9nUGlkYY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 7a:76:2e:df:27:84:6d:23:66:f6:e9:b8:9d:5a:25:98
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.31 | jq .fingerprints | yq -P`
<!-- END 81.95.52.31 -->
<!-- BEGIN 81.95.52.95 -->
## easel.webarch.net
SSH server fingerprints for `easel.webarch.net` at `81.95.52.95`:
```yml
-   hash: Bosxez6k9JZMRsrhcEpv5SEiBWmGs+jQXimahvbyAYY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 40:e8:6a:8a:ff:90:58:77:5c:58:b5:fd:40:b9:af:6e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 3IiDuqLS1s1NrbmyP/Axcw/Ax2CJuk9oOOE1g0bBlxg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: a1:50:22:e2:38:3b:51:de:a4:f5:e5:90:71:74:e8:41
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.95 | jq .fingerprints | yq -P`
<!-- END 81.95.52.95 -->
<!-- BEGIN 81.95.52.110 -->
## sanford.webarch.net
SSH server fingerprints for `sanford.webarch.net` at `81.95.52.110`:
```yml
-   hash: PYgLweDc0OxqpWU5EoMZJstv41nI4/783JhNxMsZg2Q
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 99:07:5c:26:32:a7:4b:93:a8:72:a4:60:dc:88:48:7d
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: kfC78QW5mz4F9+3eEXNKn9FeEVG/2xGlT0HZfHUFHC4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6e:b8:47:b2:a7:c8:50:a6:b5:7c:d6:98:40:a3:01:7b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.110 | jq .fingerprints | yq -P`
<!-- END 81.95.52.110 -->
<!-- BEGIN 81.95.52.96 -->
## office.unitedigitaltech.org
SSH server fingerprints for `office.unitedigitaltech.org` at `81.95.52.96`:
```yml
-   hash: VEjgyZFVotV6VWMYjQXpsakSKUh6l6vW2Xp4WBRzQCo
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: a1:9c:73:30:81:25:47:f1:5c:2b:fa:5b:ae:24:b1:7e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 5WItNm/TR83XahB39Ds6nquTFOl+5fqKQj7jFtxkACM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d9:4b:8e:b8:6e:be:9a:9c:07:ab:87:5e:c6:66:0a:57
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.96 | jq .fingerprints | yq -P`
<!-- END 81.95.52.96 -->
<!-- BEGIN 81.95.52.104 -->
## cloud.leedsbread.coop
SSH server fingerprints for `cloud.leedsbread.coop` at `81.95.52.104`:
```yml
-   hash: JSZBAi6+ifTU/B79bF6qO1xyTaoAV7tKmMetU9jTaS4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: ae:e3:93:08:d4:6d:a9:33:39:fe:1a:20:43:c0:09:7b
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 7Os6loazNRUu/iJX1iBO7/ElGh/ifFAhdPN4ExbG3u8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: fd:36:39:0f:bf:90:d2:5a:2b:00:c7:1d:38:dd:97:32
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.104 | jq .fingerprints | yq -P`
<!-- END 81.95.52.104 -->
<!-- BEGIN 81.95.52.38 -->
## imc.indymedia.org.uk
SSH server fingerprints for `imc.indymedia.org.uk` at `81.95.52.38`:
```yml
-   hash: eQRBKkcv8PRsnjNLD1xQa37UWMUK8zU1U2cITwQdDk0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b2:67:4b:0b:88:c2:b3:0a:4f:ca:12:07:f7:c9:25:bd
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: varv3fVnK/ngb/2wsHhJy+SA66tKW/hIUoY4KvrjRGk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 79:1c:00:52:b1:4b:97:d2:50:6f:8d:6c:f5:da:0b:3b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.38 | jq .fingerprints | yq -P`
<!-- END 81.95.52.38 -->
<!-- BEGIN 81.95.52.11 -->
## oriole.webarch.net
SSH server fingerprints for `oriole.webarch.net` at `81.95.52.11`:
```yml
-   hash: +gniK/FBLCamD3tWtLAkzQTuwByALmKQmuhywp82NAM
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 02:ff:2e:4a:45:2b:66:e1:72:d4:c4:a2:fc:db:c3:00
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: uvnxy0TMYybY7Zns3FtycBKEsXu1drXuZvxXl1QKvnI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f2:78:1d:a9:07:08:49:ba:50:fe:35:71:6a:c7:5b:b4
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.11 | jq .fingerprints | yq -P`
<!-- END 81.95.52.11 -->
<!-- BEGIN 81.95.52.34 -->
## animorph.webarch.coop
SSH server fingerprints for `animorph.webarch.coop` at `81.95.52.34`:
```yml
-   hash: fjdL8H/PllxWbwB36C2zMF+M3StmRZ4H+rJnsvq4pxw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: bb:32:c9:67:6b:53:bc:8d:f9:9f:30:fe:50:61:8d:de
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ImrNqGmqN9Ehg+yInqJXy5sO4LWo3k+f9/WZtLkwfSY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 17:bc:33:3b:6a:fc:50:0d:c3:2d:34:24:8f:1d:1d:34
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.34 | jq .fingerprints | yq -P`
<!-- END 81.95.52.34 -->
<!-- BEGIN 81.95.52.39 -->
## sharedfutures.webarch.net
SSH server fingerprints for `sharedfutures.webarch.net` at `81.95.52.39`:
```yml
-   hash: CqYdd+q2U4VMoQzKzRxh3Pch78A+fGLB5lDmNycWf4E
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 2b:ba:52:d1:c0:25:c8:b2:97:15:86:14:5a:aa:d1:43
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: tnkGk06XjIBYLgClOFeZK+uKlrxiETm+r9K2R92gFeY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 24:9c:6a:4f:5b:be:f2:4f:93:65:27:f2:9e:57:8a:eb
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.39 | jq .fingerprints | yq -P`
<!-- END 81.95.52.39 -->
<!-- BEGIN 81.95.52.19 -->
## greenham.webarch.net
SSH server fingerprints for `greenham.webarch.net` at `81.95.52.19`:
```yml
-   hash: CNJrrCUoR5p77jAJW9LjXKtXk64KXP4sjsAelhoIz0E
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 07:c3:81:5c:47:02:11:36:d8:ee:9c:08:29:5b:78:26
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: GpXgjZRZKwtdtap31REpbTYhjg9nkttNbkm6usKjUBI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 61:ad:e6:8b:60:12:eb:35:ff:bb:ab:34:9b:d4:6a:c2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.19 | jq .fingerprints | yq -P`
<!-- END 81.95.52.19 -->
<!-- BEGIN 81.95.52.17 -->
## sharenergy.webarch.net
SSH server fingerprints for `sharenergy.webarch.net` at `81.95.52.17`:
```yml
-   hash: vuC2J3TMSA+IOI1IW5sbdvKpa9hZDRPoCMWGI4N2/Xc
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: fc:46:d5:8c:ef:37:42:40:65:80:24:71:a1:46:5f:88
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: qfM+bq3VYzoqX7hDP8bT7Y4pNSQ/mr9AesvGDeh/F2M
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: db:9f:fd:66:ed:57:a6:47:d7:34:d0:c1:fb:34:de:cc
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.17 | jq .fingerprints | yq -P`
<!-- END 81.95.52.17 -->
<!-- BEGIN 81.95.52.21 -->
## holyoake.webarch.coop
SSH server fingerprints for `holyoake.webarch.coop` at `81.95.52.21`:
```yml
-   hash: dKG7EZCGVzPeCxRqJsJUnrpDR5JKlKCh0DsaGbfofNU
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b0:86:bc:a1:29:15:9b:1f:b1:ed:03:5a:90:eb:56:f7
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 6/3tRJ66B33vlW1UPx9Spkc6oAO3UBuAyycWKNjdXpo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 7d:e7:ac:a5:96:8b:56:63:85:dd:47:4a:68:9e:2f:1e
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.21 | jq .fingerprints | yq -P`
<!-- END 81.95.52.21 -->
<!-- BEGIN 81.95.52.59 -->
## web.cotech.uk
SSH server fingerprints for `web.cotech.uk` at `81.95.52.59`:
```yml
-   hash: rompfEXG+zhWSeef6BiSKAhka9/XpGyp2mRaMeFjoOI
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 48:2e:30:0c:0f:f4:42:ac:97:30:75:82:cf:41:0f:67
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: LsyKb7XJJhaxbxq68zm7DkLMRafU2keW3kDIyOeG024
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 08:d8:c6:65:36:8b:42:28:5a:28:a6:67:07:66:9f:36
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.59 | jq .fingerprints | yq -P`
<!-- END 81.95.52.59 -->
<!-- BEGIN 81.95.52.13 -->
## office.workers.coop
SSH server fingerprints for `office.workers.coop` at `81.95.52.13`:
```yml
-   hash: CiM08t9Ncy1kuWAzBXy16DBNcuL4kG+6gjl6XiBgYaI
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 06:c5:b6:18:32:02:da:9c:4a:b9:7b:a3:41:6f:a4:80
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 56zba/8uJ1/S9VlPFOxHyjLTU07KDxqJ/9IKdx9k9CA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f1:e8:2b:99:ee:d2:28:5f:db:14:65:b9:4b:cc:b0:94
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.13 | jq .fingerprints | yq -P`
<!-- END 81.95.52.13 -->
<!-- BEGIN 81.95.52.8 -->
## redirect.webarch.net
SSH server fingerprints for `redirect.webarch.net` at `81.95.52.8`:
```yml
-   hash: paq70SAMwMnfShpfS1V9bLJQc4E9wZUiOuTBpplPZvE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: fb:e9:16:1e:aa:3e:e9:52:62:fe:c3:b6:7d:ba:99:e9
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: qkm4WAmJrM7MBH0nqEv3G3IJYMZ+H0QyclzZQ07Lwm4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5a:07:26:8c:44:0b:26:4e:ba:a2:55:54:82:f3:ea:d5
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.8 | jq .fingerprints | yq -P`
<!-- END 81.95.52.8 -->
<!-- BEGIN 81.95.52.20 -->
## j25.webarch.net
SSH server fingerprints for `j25.webarch.net` at `81.95.52.20`:
```yml
-   hash: 5ZbIHxmXZqtg1QePzPFEPpu7DYA068WVS2RHPXu35nE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 34:10:e4:e1:33:9c:38:c2:1b:16:e4:34:da:bf:fa:39
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: TIUSHr441lWtRasQSpO45jO14+i8OiZ2oV7dUrH6cno
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8f:5e:ea:9f:4d:c5:0f:a9:b3:22:89:51:da:41:5d:89
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.20 | jq .fingerprints | yq -P`
<!-- END 81.95.52.20 -->
<!-- BEGIN 81.95.52.36 -->
## cloud.croome.net
SSH server fingerprints for `cloud.croome.net` at `81.95.52.36`:
```yml
-   hash: QRvjUS3fXSVRiLt9bupwCPhF1Xa5I5qAG7ko3Nu/i9g
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c8:ac:60:3e:b4:55:84:cc:9f:70:04:a7:6e:a6:8d:dd
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: K0hZBRkTGkrfQLo4bnr0kwyNvzZIEXtIXDslIRQfhM4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6e:b0:29:4e:68:0c:0c:1a:4c:1e:20:44:b3:77:f0:5e
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.36 | jq .fingerprints | yq -P`
<!-- END 81.95.52.36 -->

# Mail servers

* [mx.webarch.net](#mxwebarchnet)
* [cc.webarch.net](#ccwebarchnet)
* [webarch.email](#webarchemail)
* [rt.webarch.net](#rtwebarchnet)
* [sanfordmail.webarch.net](#sanfordmailwebarchnet)
* [3dcmail.webarch.net](#3dcmailwebarchnet)
* [mail.croome.net](#mailcroomenet)

<!-- BEGIN 81.95.52.71 -->
## mx.webarch.net
SSH server fingerprints for `mx.webarch.net` at `81.95.52.71`:
```yml
-   hash: TiLhGw8ethIFTBoTkh94FBG1IkK6d2qubgsFIRXPUAI
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 60:a1:a8:d9:ac:42:c0:38:56:03:d8:b3:dd:ec:69:25
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: l7rFNol/EcL/Edz1TRjh1QK1JXiCkzlEKGWsK868RPU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 2f:c9:25:6d:80:a2:cd:5b:22:34:05:6a:8b:bf:1c:e3
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.71 | jq .fingerprints | yq -P`
<!-- END 81.95.52.71 -->
<!-- BEGIN 81.95.52.112 -->
## cc.webarch.net
SSH server fingerprints for `cc.webarch.net` at `81.95.52.112`:
```yml
-   hash: 0FpptQR40N2finm0BEjZly4HldwMJ2CsV3VJtkKTMKA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b9:8f:7c:8c:d7:6c:b1:2a:f6:1c:79:16:95:37:46:28
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: m2ZKu34KbloCO4NTivv0I9/3RWpEQ54T761SYceYiis
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d9:b5:43:15:12:c0:26:76:9d:6c:0b:03:64:aa:3d:a0
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.112 | jq .fingerprints | yq -P`
<!-- END 81.95.52.112 -->
<!-- BEGIN 81.95.52.48 -->
## webarch.email
SSH server fingerprints for `webarch.email` at `81.95.52.48`:
```yml
-   hash: SDeHLmt7g8Q9bWIRJXtHtGanb9xBWlBSR1AtKDH0JOs
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 5d:91:0d:d2:d5:c3:12:49:85:f4:ec:13:ad:46:09:73
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: chvsW8hWKjKoh4YjKKNd4sT/ntTRC7uIgWbyMAh+N24
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0e:94:67:ef:00:01:4e:99:73:67:fe:99:e7:53:9f:da
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.48 | jq .fingerprints | yq -P`
<!-- END 81.95.52.48 -->
<!-- BEGIN 81.95.52.102 -->
## rt.webarch.net
SSH server fingerprints for `rt.webarch.net` at `81.95.52.102`:
```yml
-   hash: meedPtukBCv5dyxSFfiDgiqrOHePSQ2t5V6UlSSOWc8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 00:3f:7b:15:cb:79:22:8d:be:02:8d:79:18:a2:e5:3a
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: eXw/7txX4TDDUIP7NNmdxFkL8TIldhlZVtcTDul3IfU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e8:c6:ee:ba:03:f4:13:3b:44:50:5e:0a:f9:bb:0b:62
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.102 | jq .fingerprints | yq -P`
<!-- END 81.95.52.102 -->
<!-- BEGIN 81.95.52.109 -->
## sanfordmail.webarch.net
SSH server fingerprints for `sanfordmail.webarch.net` at `81.95.52.109`:
```yml
-   hash: OtkMupVxAnLYUUllScg6ELdOeAszPEvPMXWcBJXPIr8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 45:a7:52:f4:cd:77:bf:95:9a:10:b5:fb:92:6e:4c:2d
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ozvw+99TE31n68+HN1vaR8bnK/yzE9M92R9TRRlgp/A
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 2c:bf:67:37:e6:6e:0d:f1:e1:44:de:44:0a:49:29:a9
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.109 | jq .fingerprints | yq -P`
<!-- END 81.95.52.109 -->
<!-- BEGIN 81.95.52.54 -->
## 3dcmail.webarch.net
SSH server fingerprints for `3dcmail.webarch.net` at `81.95.52.54`:
```yml
-   hash: 2xzbste1rSyZE8MgE/3MK/8OCF2rpH0vGkDn3gQmZ9s
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 80:24:91:53:a9:02:84:c1:ac:ef:5a:0c:43:e3:6e:83
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: aqH4AqZGE3VN3uREhEXrTW586mQJgg01BWQnvmZFd8M
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: b8:a2:7d:9d:c6:22:08:64:bd:08:6d:26:94:ad:be:3a
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.54 | jq .fingerprints | yq -P`
<!-- END 81.95.52.54 -->
<!-- BEGIN 81.95.52.32 -->
## mail.croome.net
SSH server fingerprints for `mail.croome.net` at `81.95.52.32`:
```yml
-   hash: GJF47CNPdzde/o7sC2Zg4cP+2OxGROFGMifhH2FIZPA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 29:75:20:9e:32:7a:7c:a0:13:da:8f:05:41:f8:a2:8e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: enf740ZpBKkUEAEp0sLy5OIOmzk+GDZkAXpyd8GEeOo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 86:48:e4:bd:dd:ca:0f:1f:e4:81:57:97:80:73:63:ec
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.32 | jq .fingerprints | yq -P`
<!-- END 81.95.52.32 -->

# Misc servers

* [bert.croome.net](#bertcroomenet)
* [controlller.webarch.net](#controlllerwebarchnet)
* [proxy.webarch.net](#proxywebarchnet)
* [xen4.webarch.net](#xen4webarchnet)
* [storage.webarch.net](#storagewebarchnet)
* [backup-a.webarch.net](#backup-awebarchnet)
* [runner.git.coop](#runnergitcoop)
* [priv.runner.git.coop](#privrunnergitcoop)
* [workersauth.webarch.coop](#workersauthwebarchcoop)

<!-- BEGIN 81.95.52.5 -->
## bert.croome.net
SSH server fingerprints for `bert.croome.net` at `81.95.52.5`:
```yml
-   hash: mPZCheFmfioVhhYrmtFcWswVAJKThXMkgprI7UE7EGY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 2a:35:06:ad:fd:37:b0:d9:2f:bf:e9:d7:b3:24:0d:cf
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: nVgvxb1YK/pGjLIIKMgmbIG4b9DqFNN2gjh2W9IlC60
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 62:83:14:ed:c8:fe:dd:32:4e:9d:75:48:a6:90:2c:ce
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.5 | jq .fingerprints | yq -P`
<!-- END 81.95.52.5 -->
<!-- BEGIN 81.95.52.29 -->
## proxy.webarch.net
SSH server fingerprints for `proxy.webarch.net` at `81.95.52.29`:
```yml
-   hash: 77II+yq10bvyH8/ZSIzbVXHIcoEx0aCIGBF0c2gqrI8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 2e:ee:ba:d0:fe:22:6f:01:50:c4:a3:26:8f:fd:bd:ad
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: DtN+vCH86Stf575Vc3bE/KG79GebjcTF3r+pTXSPg7U
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 45:b1:7b:22:82:95:d5:e0:44:9b:2c:33:11:ab:28:7d
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.29 | jq .fingerprints | yq -P`
<!-- END 81.95.52.29 -->
<!-- BEGIN 81.95.52.35 -->
## controller.webarch.net
SSH server fingerprints for `controller.webarch.net` at `81.95.52.35`:
```yml
-   hash: wtypAGZtUWiN7JUKy33FNPSlbjablQ16UrMEXEcSsBk
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 11:2e:56:15:be:23:58:98:eb:06:43:c0:6a:3e:9a:c3
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: QhgNOwfb79pauiKhCEI1VsfYs9KYe140O+BnY3UOOIE
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6c:07:2e:6e:e8:6d:bc:a6:50:95:26:79:5a:31:1e:a2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.35 | jq .fingerprints | yq -P`
<!-- END 81.95.52.35 -->
<!-- BEGIN 81.95.52.121 -->
## xen4.webarch.net
SSH server fingerprints for `xen4.webarch.net` at `81.95.52.121`:
```yml
-   hash: p0rWRNs23UpPMGZI+N9/H5CI4SQlBFRd+4QLcxtbjHM
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 79:1f:6f:1a:45:c0:17:53:43:33:4a:b6:86:74:57:aa
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: zQbQlMJqdET13m7+YKMZYYK5sfbDZYFF5AJR4FD/oKI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: cc:d7:e4:a9:95:cb:b1:8d:ca:70:e3:20:6e:6d:c3:1d
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.121 | jq .fingerprints | yq -P`
<!-- END 81.95.52.121 -->
<!-- BEGIN 81.95.52.125 -->
## storage.webarch.net
SSH server fingerprints for `storage.webarch.net` at `81.95.52.125`:
```yml
-   hash: ljf5za5GBODi+pEIDu2QDgB5fSiStMpdPxmLD8nx74U
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: d7:59:58:32:b2:11:54:18:f8:34:0e:94:2a:c3:ab:70
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: nZenAHPCkA2/klKdtDk72HbKgNpyfTRXACxYxUsQMXI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 15:ba:1c:3e:34:4b:8c:4a:84:61:35:ea:1f:02:f3:d2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.125 | jq .fingerprints | yq -P`
<!-- END 81.95.52.125 -->
<!-- BEGIN 81.95.52.122 -->
## backup-a.webarch.net
SSH server fingerprints for `backup-a.webarch.net` at `81.95.52.122`:
```yml
-   hash: ho+pmno1beyuLvvLe8Wr2AyIR9HdRjPA2uUQ4UxbVRE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 8b:68:74:3a:85:be:71:93:fe:10:74:31:61:21:31:b0
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: aQoT/1jf2gMDCzgHzu+1r8Z0GCnPsQdzHipEhJ1hqaQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 71:2a:02:10:6e:0a:ec:57:c9:d9:f8:2e:84:64:45:fa
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.122 | jq .fingerprints | yq -P`
<!-- END 81.95.52.122 -->
<!-- BEGIN 81.95.52.69 -->
## priv.runner.git.coop
SSH server fingerprints for `priv.runner.git.coop` at `81.95.52.69`:
```yml
-   hash: ckErqjjf2DCCN76S/S/wRBVpGmABKuMWxQ966EYLHiw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 99:74:c8:51:6e:42:a8:f8:a0:2e:f8:7b:5c:b5:cb:60
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: NEs73xGPVOozfW6Wz8yFcVcePJumzoSQ1WwX/gOMaEw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5c:7e:c2:4f:d6:27:41:5d:1c:b8:9d:8a:9c:2f:a6:dc
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.69 | jq .fingerprints | yq -P`
<!-- END 81.95.52.69 -->
<!-- BEGIN 81.95.52.70 -->
## runner.git.coop
SSH server fingerprints for `runner.git.coop` at `81.95.52.70`:
```yml
-   hash: hm0BUU7506/aH+NhMG6x6evB1BOU9QtzlOMMLnUube4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 3a:8d:24:2f:ca:a2:d0:5b:d3:73:de:dd:00:e3:ec:b8
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: PfpDXsRgShHtEumiIbt3I+xpNsD0hiN1ThaVlYzK6Uo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: cd:79:75:07:b1:13:49:08:71:3d:a8:e8:ab:b6:96:e9
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.70 | jq .fingerprints | yq -P`
<!-- END 81.95.52.70 -->
<!-- BEGIN 81.95.52.9 -->
## auth.workers.coop
SSH server fingerprints for `auth.workers.coop` at `81.95.52.9`:
```yml
-   hash: dWC+H39wPb9e3LJaD8yR25XekuIJ0WGiVu/hm6HPj7A
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 64:8a:14:f9:ed:e5:bf:e0:96:79:75:0f:c4:28:ed:b4
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: nE5G0OVbRFAnkLRhZDrcx0mkUPUPpbONoBqiTwKUzeM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 2d:e7:3c:5a:ce:0d:d4:7d:52:e1:36:34:d9:b7:c6:70
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.9 | jq .fingerprints | yq -P`
<!-- END 81.95.52.9 -->
<!-- BEGIN 81.95.52.41 -->
## creative1.webarch.coop
SSH server fingerprints for `creative1.webarch.coop` at `81.95.52.41`:
```yml
-   hash: Ztbn+rGa3HTY+NHlcHC4N6aYpQapqWvWmCQAUsvCE7k
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 72:59:e2:38:ae:ab:27:c4:e5:54:d2:12:f0:59:b7:60
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: iC4fmmAMmMZZrqBIErGuOoJZOctPXHyJ8cz+I8nrby8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 39:c1:21:38:99:a4:d7:86:af:eb:c3:71:47:aa:2d:fb
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.41 | jq .fingerprints | yq -P`
<!-- END 81.95.52.41 -->
<!-- BEGIN 81.95.52.7 -->
## chat.workers.coop
SSH server fingerprints for `chat.workers.coop` at `81.95.52.7`:
```yml
-   hash: OkW76rzqhra103eS332QFx6IOjcLi9DIDoKAWKkrpAE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b5:e3:e0:b6:77:4e:1b:9c:81:d0:90:ed:16:37:c8:00
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: e03XfmziVFFeK3vRsXOfeZs5MJk9GXYVfbxu2pGKpM0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 36:bd:70:7c:fd:b9:03:91:f3:e1:00:32:bf:07:e6:0b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.7 | jq .fingerprints | yq -P`
<!-- END 81.95.52.7 -->
<!-- BEGIN 81.95.52.45 -->
## synapse.webarchitects.org
SSH server fingerprints for `synapse.webarchitects.org` at `81.95.52.45`:
```yml
-   hash: Ss6wJFyPVOcZqai6JSUsrtCeVs7mpZvhCwdlvBYH6EY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 7a:b0:13:5a:ec:8d:f7:22:a0:a4:1b:c6:58:f0:fc:bc
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: v9Vogl7sfooK1q6/rbL994mc/tvhJq/tcQzrUprAluk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: fe:59:b6:09:cd:ac:ad:bd:ba:2a:8a:ce:b0:25:79:ce
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.45 | jq .fingerprints | yq -P`
<!-- END 81.95.52.45 -->
<!-- BEGIN 81.95.52.91 -->
## mastodon.webarch.org.uk
SSH server fingerprints for `mastodon.webarch.org.uk` at `81.95.52.91`:
```yml
-   hash: vbQQgG6PCLbIMGQ48o2cxsVE1ZjAQYpMjYY+PjPBo78
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 65:30:34:43:e3:e4:f3:a8:9f:1d:ce:c3:c7:b6:21:ef
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: UPvSlF4s7E6F64ftHB7Xd8OigVYftEX59ktadt1Gclk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 9f:64:88:95:e6:86:09:d9:21:2d:64:15:f9:0e:f9:43
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.91 | jq .fingerprints | yq -P`
<!-- END 81.95.52.91 -->
<!-- BEGIN 81.95.52.94 -->
## gicast2.animorph.coop
SSH server fingerprints for `gicast2.animorph.coop` at `81.95.52.94`:
```yml
-   hash: 8LbOE2/jCAEpzeLKIDl9CtfPvwbCsdglLoqkHvX3IMc
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 0e:4c:68:18:2b:15:b6:98:54:9f:f7:d2:5f:1b:ad:95
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: i1oGVR9YXC7ypnm5k+/VyMA7etBLy3JkIhUE4BAYUWs
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 30:1a:42:5d:96:3b:60:69:32:a5:30:a8:22:17:7f:00
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.94 | jq .fingerprints | yq -P`
<!-- END 81.95.52.94 -->
<!-- BEGIN 94.199.30.35 -->
## harland.webarch.net
SSH server fingerprints for `harland.webarch.net` at `94.199.30.35`:
```yml
-   hash: 5Ikcbair6vZzFJQKMrshmRrp1H7eBRTIxdq3Y59x7ho
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 46:11:f6:19:26:d9:7d:b9:55:e9:37:4f:4b:b3:43:9d
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: vWc1rWlkiFem6XkTgYmVuj7J+p8GuwgcPybcRuT41L8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8a:b6:df:a3:f9:dc:93:e7:47:64:2a:f9:c7:0e:1b:07
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 94.199.30.35 | jq .fingerprints | yq -P`
<!-- END 94.199.30.35 -->
<!-- BEGIN 81.95.52.16 -->
## onekind.webarch.net
SSH server fingerprints for `onekind.webarch.net` at `81.95.52.16`:
```yml
-   hash: iuvTbuNdpKcO+YcjIYqErar/JSdnZseUy7aB5ktJ4YQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 3f:27:ad:ee:cc:0a:aa:9d:fc:28:49:47:0d:87:13:16
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: /yLwDChPF8SW9wm45CqJofenaX2GN6Ud/akF68vNP9E
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 65:96:6c:93:2b:78:8d:14:36:11:45:b9:0f:89:d5:09
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.16 | jq .fingerprints | yq -P`
<!-- END 81.95.52.16 -->
<!-- BEGIN 192.168.8.2 -->
## harland.webarch.net
SSH server fingerprints for `harland.webarch.net` at `192.168.8.2`:
```yml
-   hash: 5Ikcbair6vZzFJQKMrshmRrp1H7eBRTIxdq3Y59x7ho
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 46:11:f6:19:26:d9:7d:b9:55:e9:37:4f:4b:b3:43:9d
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: vWc1rWlkiFem6XkTgYmVuj7J+p8GuwgcPybcRuT41L8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8a:b6:df:a3:f9:dc:93:e7:47:64:2a:f9:c7:0e:1b:07
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 192.168.8.2 | jq .fingerprints | yq -P`
<!-- END 192.168.8.2 -->

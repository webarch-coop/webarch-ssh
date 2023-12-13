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

It should output the version of OpenSSH that you have installed:

```
OpenSSH_9.2p1 Debian-2, OpenSSL 3.0.8 7 Feb 2023]
```

Check that you are running [OpenSSH 8.2](https://www.openssh.com/releasenotes.html#8.2) or greater as this version (which was released on 2020-02-14) added:

> an Include sshd_config keyword that allows including additional configuration files

Check that you have `git`, run:

```bash
git version
```

It should output the version of `git` that you have installed:

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

And then either manually add the following line to to the top of your existing `~/.ssh/config` file:

```
Include ~/.ssh/webarch-ssh/config
```

Or run this command for the file to be created with this content or the content to be appended to an existing file:

```bash
echo "Include ~/.ssh/webarch-ssh/config" >> ~/.ssh/config && chmod 0600 ~/.ssh/config
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
-   hash: FxkEors9uuUTSkNHvTqNt8wpUzBlMQbkK/cXDp9uFDQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d4:b6:7d:1e:47:33:f3:67:d3:de:83:e4:ca:42:02:b5
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
-   hash: 7cg8eTYZDZKM/gmkPWs2XjnQX6EfqRrXSB3TJkTXXJQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 60:18:e9:2c:8b:40:8a:a5:06:09:98:d5:a0:fc:09:2d
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
-   hash: ECEyDne5sJESb/I86p+W6RwEMa1vhA7ZS7mq/ZACmb0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 90:64:c2:22:37:66:61:79:ec:a5:d0:af:62:f2:87:bc
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.42 | jq .fingerprints | yq -P`
<!-- END 81.95.52.42 -->
<!-- BEGIN 81.95.52.26 -->
## nextcloud.webarch.org.uk
SSH server fingerprints for `nextcloud.webarch.org.uk` at `81.95.52.26`:
```yml
-   hash: DQSOGewK/5fhhb6OSWf1oTcdqI4IvH0cvHkXga/Ot+0
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 7e:fb:dc:d2:82:1e:b2:66:05:50:4d:8f:f7:c2:f5:20
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: NoSx/6ps0iakC/4gkjkzS/JHU1Tk160mVtuifR1K044
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 1d:0e:e9:45:d0:3c:c7:57:18:ce:9e:fb:cf:52:a7:1d
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.26 | jq .fingerprints | yq -P`
<!-- END 81.95.52.26 -->
<!-- BEGIN 81.95.52.88 -->
## onlyoffice.webarchitects.org.uk
SSH server fingerprints for `onlyoffice.webarchitects.org.uk` at `81.95.52.88`:
```yml
-   hash: mGL7cDJVZm/968HWFH6c9lF0T8ZAHBcnMl4twLsE4/o
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 96:b2:58:1d:d3:84:d9:39:de:df:7a:04:ee:9b:1f:1c
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: BW6ZLEJLkA9YzB+OdUdlTUHx6KORnGs1L9uCJMOCnEo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6c:1e:e2:4c:10:28:b0:45:15:f4:7c:ac:38:40:6d:c2
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.88 | jq .fingerprints | yq -P`
<!-- END 81.95.52.88 -->
<!-- BEGIN 81.95.52.56 -->
## wsh.webarchitects.org.uk
SSH server fingerprints for `wsh.webarchitects.org.uk` at `81.95.52.56`:
```yml
-   hash: E3aGMSfTsJ/q37XLNJBCqxhFxdeVOiejDn60bZxZPIg
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 2e:74:f3:80:ac:fc:57:89:66:88:91:2b:f1:d1:42:92
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: kGoLz6Kb6ocCcwnTqAPB0Yvi6WOLj0xBsNFNzBs/p4A
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 09:fd:93:8d:8a:4f:62:c5:c5:dc:2c:cb:41:e5:c9:ed
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
-   hash: 07lBduPOCl8uDfijwRvJ8QcYsiWhtfP1JOGQuNX7mDk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f6:93:4b:a4:1c:08:00:dd:41:3f:70:25:b9:1b:a0:1b
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
-   hash: R7glUNE25m0DOkFoqtFZTqZW4Y/IqidzJwiZamIMbgY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 18:8c:fe:0a:e8:87:e5:e4:b2:91:87:29:12:6f:62:e9
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
-   hash: C4hOI70xC1t7Tanwjylz955cJ9xuadHZlWRMUn/wYps
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 95:52:7c:57:c2:f7:a2:5d:84:ff:01:c6:37:d2:36:c5
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
-   hash: jTB7q77jylAiPwaen657qQHml1Uj8G4cq8VMGm7aBtM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f0:05:07:ab:e3:17:f0:f5:1c:12:e4:7e:9f:71:1a:d7
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
-   hash: OLppt6wjR81ocTWqT3BX2dhogJRmhjC6jWO/YqeKl0Y
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 7f:c0:02:39:cf:33:99:d0:87:61:21:96:d5:a5:81:69
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
-   hash: XL8GPOy1zfrH8Z6ab2SxCGRZ7gWSZI21fmSwAqooBaU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 96:a9:ee:22:02:9c:5d:04:22:9c:12:67:0e:1f:ef:3a
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
-   hash: 6ePClOSMjiRCdsaI3ryBRVEKoFnvpEds7bF2yn9Uzu0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 98:d3:31:4c:6b:ed:93:3a:81:54:5a:34:28:94:eb:4b
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
-   hash: S2RHkA3y9ITq0SsZz7mu/jcft2dohhmu4xcgjExbb3M
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bd:96:94:11:b0:8e:f5:e6:cc:12:fc:c0:3a:cb:9e:fe
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
-   hash: Nuk0YiPegQDod7EZDQwtYNlP7c2i3qEk+peuN6Cmoh0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e3:41:59:17:7f:77:1c:1d:42:ba:a6:76:70:df:29:b6
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
-   hash: WJWkiZRxLWLOmvrBHJ53yeThKNGEMhO33AgR/G4I4y8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 03:e6:28:07:29:b1:8f:c5:32:e3:f1:3d:93:f4:71:dc
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
-   hash: HbolIROj/VjrE027QPITy6R4DN0tkutI9QxbKInOQyk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: b5:64:f9:99:67:a0:27:de:f2:16:f7:23:27:2f:4e:eb
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
-   hash: hAMVczxYzQSfjrW5LgJmruE304jXkmcOytnZayNlrjk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ea:68:da:82:8f:71:ba:31:f9:e4:80:f5:ee:b2:29:04
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
-   hash: YzPw7IGX4cZGZq9VqC+9pn+Ieq2PUxBEtZPplJsLFio
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f7:66:ec:db:70:4b:93:42:98:77:57:3d:cd:32:1f:fd
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
-   hash: eUDpOa3Vh1kNDvk5sK4rHwo7Gd1FVRIU/cDbaiAK7Hs
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c6:a9:d7:5c:30:0b:9b:50:eb:ce:c9:f6:8e:a2:68:0b
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
-   hash: G2ONIBtMeP3ZPpvGeb/Qijr9GE4+X5khKwRa50tT2lo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 31:ae:d5:ee:1a:ec:12:09:e8:13:16:44:8f:7d:39:56
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
-   hash: pE0W6GRkVIoMu+e8hl0W5dvtIZA2dLBrSmaOtaAcR3M
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 93:27:eb:ba:c6:64:0a:39:e9:6c:54:cc:07:7b:41:69
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
-   hash: cyykOyHE7B/5CGGPc+gBWFwIXb3VwqmY+/iVs0jYj0A
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e4:7a:42:73:7f:9a:1f:18:03:87:e7:82:db:02:26:c6
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.54 | jq .fingerprints | yq -P`
<!-- END 81.95.52.54 -->
<!-- BEGIN 81.95.52.32 -->
## croome.email
SSH server fingerprints for `croome.email` at `81.95.52.32`:
```yml
-   hash: GJF47CNPdzde/o7sC2Zg4cP+2OxGROFGMifhH2FIZPA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 29:75:20:9e:32:7a:7c:a0:13:da:8f:05:41:f8:a2:8e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: zzrbPSwViKJNs7DvZ73jQbTlgMzps6/vIY1DfyRC+GE
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c4:56:e6:3f:ab:58:b5:00:ed:85:9d:b7:b8:0b:65:ca
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
-   hash: nkBI7gUEPffowlGFExyoGYNNceUwrNX5nuZnySaurOc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 16:bc:66:47:26:d7:fa:c4:2f:83:19:ad:ad:a4:d7:2b
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
-   hash: 8g8mrdumVAiQ2JhHmFFNzRfv8OhOLDMQJe3YOeGbF28
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 4a:29:33:b2:1c:38:54:13:ed:e0:ce:bd:93:75:ac:f4
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.29 | jq .fingerprints | yq -P`
<!-- END 81.95.52.29 -->
<!-- BEGIN 81.95.52.35 -->
## control.croome.net
SSH server fingerprints for `control.croome.net` at `81.95.52.35`:
```yml
-   hash: wtypAGZtUWiN7JUKy33FNPSlbjablQ16UrMEXEcSsBk
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 11:2e:56:15:be:23:58:98:eb:06:43:c0:6a:3e:9a:c3
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: W/FEv74QvWSJzQbatjemJlz5sRVI6KGEnXy5ekx4+OM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 60:93:9c:6a:46:85:79:00:03:48:0f:1b:ba:66:56:53
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
-   hash: aPBhW8ksO2SqHemceYtdPXr/lTIPhMXjJMHXa0+xcRA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e9:70:00:b8:71:88:00:d8:c2:ee:aa:e1:d1:6c:7b:f1
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
-   hash: hwa0B4F9OH/GvcjFYYdST1ybQkYbH8yoU66pYmTQIuA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0c:9e:74:df:5c:17:2d:3a:da:c2:84:20:08:c8:b6:6e
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
-   hash: PowWENwITIllBPTl03y1LvxOigrlBPwllAhxBAmwkdA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e8:6d:58:30:90:e1:0d:ad:c7:15:ae:5d:9d:dd:35:da
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
-   hash: ny0f9ojFR1/1Y/o/YZCrp0rv0SmX/8xuoKzFk+RZIyw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: a8:eb:cb:15:71:f0:8f:07:39:a1:76:2c:3a:60:74:e3
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
-   hash: wSwLutMP3dG/t1N5XmC5myvikpbRK7wlBbOH9dUuqwg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f6:8d:17:f1:09:2f:7d:a5:c9:ad:8c:e9:e6:e0:cc:df
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
-   hash: zDYfOCzsqp3KSQjzdOY9yDmr70ha0mWPnWw+CvOeBe0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 40:f9:ea:9a:34:df:c5:70:c7:87:be:dd:49:8a:9a:65
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
-   hash: ROngh3AsqyojBqaWcnvRRn/Vg3oaEmoxKjzTrPbEfcQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f7:c6:24:fa:6d:23:e2:f5:b4:89:42:a3:ec:34:e5:1c
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
-   hash: Pj+4dQ7zCCjhzzaUBl45WHWo87dvXjSt+FHv66NjGUs
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 9d:c5:9c:d7:b8:30:ad:30:68:cc:5f:8d:68:d0:95:b1
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
-   hash: 3Sp/dACyQZOx0e62TVfg3JlQIM2RG9iGXZ3tfQFBsfM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 71:3c:bf:3a:ab:e7:03:f1:10:25:49:f9:88:61:91:6d
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
## cal.workers.coop
SSH server fingerprints for `cal.workers.coop` at `81.95.52.16`:
```yml
-   hash: JYvPmtuBr1/1ifZhLUEkX0xtz7ABhAyhalVPg061kzE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: f5:53:0f:99:9b:37:ce:11:92:46:e0:59:9e:5c:d3:02
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: QfQIOPfFSEsbHdpKEGdI+FSrtZSpdrnhnrBuZpJ25iY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8e:ad:d8:a6:35:98:48:60:2c:2a:4d:79:ae:18:76:89
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
-   hash: ZSK26Rvwh4E5yyRxqf4fQkRKHhMXvwfjE4a9HmRcJoA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 80:25:46:78:16:24:a8:b2:dd:84:aa:ae:c6:d9:bd:f6
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 192.168.8.2 | jq .fingerprints | yq -P`
<!-- END 192.168.8.2 -->
<!-- BEGIN 213.108.108.167 -->
## greenhost.crin.org
SSH server fingerprints for `greenhost.crin.org` at `213.108.108.167`:
```yml
-   hash: JGo6Nu5hkBF9iZaBqED1rBKUpuKBklAF7HSYtXGeTJM
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: e7:2b:ca:c0:02:ef:d4:01:e8:34:a2:42:bf:e0:ff:1a
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: D8cMmHWKzP6QarPGAFDpKhO0beLz3SZSJhPs1QRF7BY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bf:01:00:91:a8:e1:e9:31:c3:c6:55:ca:d7:03:4b:29
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 213.108.108.167 | jq .fingerprints | yq -P`
<!-- END 213.108.108.167 -->
<!-- BEGIN 81.95.52.72 -->
## op.animorph.coop
SSH server fingerprints for `op.animorph.coop` at `81.95.52.72`:
```yml
-   hash: QCobd7415j56hnv0Wxil0RoCQyXoL3AKioK+rdLV/II
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 7a:4a:d5:a6:36:12:8d:b2:c7:fc:e2:fa:e7:dc:8c:23
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: dDp2LhfcT+mlbl/Q2f7oDZNc4QzJk475ajDZwpWMRqg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: fa:36:f9:7f:43:20:f7:8f:1b:6a:ff:c5:b5:fb:70:7c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.72 | jq .fingerprints | yq -P`
<!-- END 81.95.52.72 -->
<!-- BEGIN 81.95.52.78 -->
## together.webarch.net
SSH server fingerprints for `together.webarch.net` at `81.95.52.78`:
```yml
-   hash: 1iiIdz7f1ubE/BV6tAbgsNCtBmfpnngH3XsMNYESntc
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 42:68:89:c1:eb:6b:61:08:9a:2a:98:e0:c8:66:df:05
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: DWdY3TEwXznf4NzLr4dpAyqrMKG7eSR3U1VHgdGwrAo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0b:3c:06:51:1e:4e:93:b2:bf:80:b7:f2:98:23:49:4e
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.78 | jq .fingerprints | yq -P`
<!-- END 81.95.52.78 -->
<!-- BEGIN 81.95.52.73 -->
## mailcoop.webarch.net
SSH server fingerprints for `mailcoop.webarch.net` at `81.95.52.73`:
```yml
-   hash: GK5EXH7rYk+sI6uJPkvXFaFy4mab7o8eCxAMz81/DY8
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: a2:5a:2e:b9:da:ed:cd:15:42:5b:4b:6b:b4:c0:d7:c4
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: Vdubr/67ra40osSrBqoeLvqlCMGtUi66OG5hSXem6lc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8a:a0:1f:4e:59:9d:ef:c5:b0:0f:d7:0c:9b:32:c0:69
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.73 | jq .fingerprints | yq -P`
<!-- END 81.95.52.73 -->
<!-- BEGIN 81.95.52.97 -->
## red.webarch.net
SSH server fingerprints for `red.webarch.net` at `81.95.52.97`:
```yml
-   hash: 2mGW3nxUiSI2smLH2tZMJVy3frvygTfFzMhJiLXWLSw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: ce:43:49:0d:69:59:8a:80:d7:fa:5d:84:8a:d8:0a:c2
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: JJfCZMnJDQQySWgEOpnxf1TfZrXxjLdDBCEmPv84G+4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 35:ce:bf:88:29:93:43:a4:a6:82:17:55:b8:85:a5:78
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.97 | jq .fingerprints | yq -P`
<!-- END 81.95.52.97 -->
<!-- BEGIN 81.95.52.74 -->
## sw.animorph.coop
SSH server fingerprints for `sw.animorph.coop` at `81.95.52.74`:
```yml
-   hash: +c2M9DBZu9kIY3a1E6qpQ7SqyXtCSAbW2rQ75t/diWQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c0:98:61:65:d1:ab:04:96:4c:f7:97:94:a0:93:c1:33
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: f85gSNoC8Nr+pJZpq94ZI7fsQjozgYDfZlSgUAUz9Zo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 03:4f:1c:06:25:5f:fd:d9:dc:dd:5d:d9:2c:48:95:c1
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.74 | jq .fingerprints | yq -P`
<!-- END 81.95.52.74 -->
<!-- BEGIN 81.95.52.75 -->
## workspace.webarch.org.uk
SSH server fingerprints for `workspace.webarch.org.uk` at `81.95.52.75`:
```yml
-   hash: 2RjWRdXMf5JYyrpqYS9pRAc/6c7nQ1CY43nxTIZ1dno
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: bc:5a:9e:02:65:5e:fb:61:b1:3a:8a:9f:a3:af:34:69
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: KmyGM8e32PiePCg4AHnV0U33PCAcQgbm2bZC9H3Y1XU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f9:9d:3b:43:7b:16:e3:b5:ed:98:86:f6:ce:79:50:a9
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.75 | jq .fingerprints | yq -P`
<!-- END 81.95.52.75 -->

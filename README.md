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

Open a terninal client and check that you have OpenSSH, run (note this is a uppercase `V`):

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
-   hash: ZqMuNmoV9dPBJjQn26Q8TeGasfJkBltarCUOM559RH4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e1:1a:28:c9:d8:36:34:25:03:e5:03:37:18:5a:82:d0
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
-   hash: owmQMQEVZ7MVhA/rlCnPO1GMxlthVVGG0s4b/uoFIOQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 32:56:c8:2b:69:ae:4c:b0:90:05:3d:9e:26:0b:01:4a
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
-   hash: VaoaOurV0JGnGiipwm/hlB3AxN28625Qk9+16UiVS0Y
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ef:54:07:a0:b3:b2:27:6d:bb:8b:0e:eb:e1:1a:98:be
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
-   hash: 30gvg7gaw90UdMVbCNQYp21oWfa5kRhiRdyTzyjgOm0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: d1:36:9d:3a:04:9c:5b:a3:89:5f:8f:bb:52:bd:8f:11
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
-   hash: 77mOLoVV4p2DNwYwAFk2rT3HPFUZobiPAErdx+IbG3k
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 30:a2:a3:b0:3c:c8:79:c0:6e:05:72:8a:d9:44:66:14
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
-   hash: EyDlrEZ4BhoYXt78MV7RQatNZ/8NYR/qwg1N0F2WeHQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: af:f2:0b:15:32:bb:6b:2e:2f:13:3f:99:f3:b3:63:25
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
-   hash: Q5U1/ch+kbZeOMPB4+cWo+RhK0UGGWozg16Hbgbp/dI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 67:27:93:11:c8:bf:f6:3d:70:e0:3b:31:d0:6e:7a:85
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
-   hash: 7yyIiIjUcFaHMlQYCtyEMb9oFBDo+1dwe0rMMwa+Rdk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 91:97:fb:55:f3:37:73:94:77:43:29:fe:28:f9:88:fb
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
-   hash: 8A7T2UN/UC2AVpHP2YCacfD7uspycnjABZHjuAgcQV4
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c0:1d:d9:49:32:c0:04:a0:9f:69:1a:18:e8:8e:c5:af
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
-   hash: swqcHiOjI1IrO139QqObwtwRDS3JuWoDvbWcTbfoMYQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 52:86:7f:e9:d4:ae:a2:72:b7:9c:d5:7c:dc:54:a3:ba
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
-   hash: kF10X8bdmNLhWar1xC8lp8jpzSpxKN8T87wgJtDNhdg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 42:d2:79:e6:56:85:2f:41:58:2e:8d:63:6b:a6:9f:6f
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
-   hash: KVUm+m/hhVmj8jnZSJQ0u1nX0XvPN3krJdAOYKG2xDw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: b7:5e:5e:2c:6a:6b:2a:26:25:87:8a:6a:f8:f0:dd:e7
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 185.112.146.79 | jq .fingerprints | yq -P`
<!-- END 185.112.146.79 -->

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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.26 | jq .fingerprints | yq -P`
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.88 | jq .fingerprints | yq -P`
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.56 | jq .fingerprints | yq -P`
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
-   hash: roKSXNtPc6klRREAR/Ri5+DbtCimeVk+JKI1/GS5yRM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 1c:95:c5:ed:d1:9e:2d:85:cc:16:25:dd:e9:14:1f:6d
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
-   hash: ZfrUZQmk18rSF48chBERdvI7LhUPNDMfpds2pF5/z5s
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 78:d7:12:08:22:ad:a2:8b:cb:0e:40:98:b8:2c:4c:24
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.87 | jq .fingerprints | yq -P`
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
-   hash: EaGvZRZmA5nyGXW/WoTHETNpG3wyOfjHw6FOaFCogQ8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 25:6b:a1:6e:c1:c0:db:05:a8:31:8f:2f:be:20:d5:6c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.90 | jq .fingerprints | yq -P`
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
-   hash: 6NBH8kn/Bk9B24ulQam8W0LLqGsIYOHjAQ5VYMmDZoA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 99:18:9f:65:5e:d7:49:c0:d2:91:79:5a:37:4f:e5:2b
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
-   hash: /XK8kzz0031KaXKh5T3EsNBmbFQdYfm7df7mC9pd99g
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ca:62:ae:35:53:a1:1c:eb:56:93:5f:e7:b5:ca:d6:b6
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.100 | jq .fingerprints | yq -P`
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
-   hash: vWRcInj4WZF232aKwLK2/m35DgC1bxvgJiHgskBdPd8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 06:96:e6:b2:14:18:c9:a1:0b:a2:10:58:e7:fa:5e:ac
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
-   hash: vWu2fLth+NNIVxgmoSJoBehvLPtxZdfgkpDviF9XTiA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 25:e8:bc:f7:c7:51:4e:15:94:1f:44:3e:27:c0:79:81
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.14 | jq .fingerprints | yq -P`
<!-- END 81.95.52.14 -->
<!-- BEGIN 81.95.52.55 -->
## 3dccloud.3dcampus.co.uk
SSH server fingerprints for `3dccloud.3dcampus.co.uk` at `81.95.52.55`:
```yml
-   hash: hapOsjA3THlfM4EY4ZW3golYY1mNOu6u0ntV9J5EC3Y
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c1:9e:e6:68:96:91:22:4f:52:da:5b:bf:9c:fe:56:49
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: jdhbmDz4w9PjppN1r0DE24zcwX2JTz3+6OPYp7UzdmE
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 73:c3:09:a6:c8:bf:31:00:71:de:8a:cb:eb:ed:b7:e0
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.55 | jq .fingerprints | yq -P`
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
-   hash: I34pzTaDuqpxXyPpKHpRWL1EzI+oqdul8OmNPy5E8kU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: e4:52:ee:db:40:91:49:7e:b5:47:43:07:6b:dd:64:8d
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.43 | jq .fingerprints | yq -P`
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
-   hash: 37eITUDwho/L59Y2jL6+izKU+ch3hRXcOJdHosapoNc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 47:24:67:20:e3:6c:15:b4:f0:28:c4:a7:60:6c:2c:29
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.103 | jq .fingerprints | yq -P`
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
-   hash: 414wOCEE5qwld2MQq3GHq6ebeMptegRomO20ZITmRX8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: be:b8:9b:43:f9:92:0e:f3:ea:ce:c6:c5:c0:84:b0:6e
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.31 | jq .fingerprints | yq -P`
<!-- END 81.95.52.31 -->
<!-- BEGIN 81.95.52.95 -->
## wao.webarch.net
SSH server fingerprints for `wao.webarch.net` at `81.95.52.95`:
```yml
-   hash: ZA7BRSof65HGpcU4jiAbzOWeFbQjDjtShw7B1rny3kQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 15:6e:78:31:8e:39:01:bc:8e:bf:88:e1:ff:69:c9:ed
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: IhJ9jdywVKHzaiRhezuhrrYWcXtjAa+m6mswVjWyyrM
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 9c:91:47:0e:0b:e7:5a:06:af:82:32:79:96:94:e8:cc
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.95 | jq .fingerprints | yq -P`
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
-   hash: 6KoraUZy6nn2nKGhvRevz8y657867AQEUDZvqu4Bf8Y
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5e:24:01:06:06:75:ba:bd:5a:90:7b:0f:60:1b:fc:db
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.110 | jq .fingerprints | yq -P`
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
-   hash: LIsnGAfyhrC2lgoVM92Dni00L24nhPcfv/M0lcel3/A
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 31:d1:82:95:f7:0d:d3:6d:9c:38:37:8a:02:d4:15:fa
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.96 | jq .fingerprints | yq -P`
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
-   hash: IWT4AOGZaZ548DzDlgGrifw//5e8Z55aN5MHqivOYsc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f1:d1:a8:5a:ac:0c:3f:f7:02:b0:4a:52:11:31:0a:9f
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.104 | jq .fingerprints | yq -P`
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
-   hash: XKv886VY4zUKuGQVQwGWxkMQUifNNxgSLoEg8GS8ahA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: ae:fe:01:a6:54:cb:d9:32:3c:fb:11:6f:3a:84:e6:aa
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
-   hash: zJxieTWdGM56WDAMj79bM6mFAuVrG8E2j1yvSo9DjTQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5a:44:b6:93:e4:6d:fd:66:25:d1:20:68:52:ec:85:0a
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.11 | jq .fingerprints | yq -P`
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.34 | jq .fingerprints | yq -P`
<!-- END 81.95.52.34 -->
<!-- BEGIN 81.95.52.39 -->
## sso2.meet.coop
SSH server fingerprints for `sso2.meet.coop` at `81.95.52.39`:
```yml
-   hash: 48+qEoVYaHQEqVsIPOmg3pxaVlBTS0NJ1upJQ0L8b0U
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: a7:c4:be:40:3c:7e:6c:27:a8:4c:31:df:b2:b0:6a:c0
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: e3cznX7fMim/tWedN9FrD70IdHJ2k5eaxA6knbNWDOY
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6d:83:d2:77:a8:a5:f6:83:83:d7:0a:8b:8c:02:a4:6b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.39 | jq .fingerprints | yq -P`
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
-   hash: GRJawuMDVxyepNFpcBaP0vYjLRoOPNGY7WhFv+zHq3A
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6e:26:9c:c5:39:b2:74:84:7b:19:c1:99:9c:a2:ac:9a
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.17 | jq .fingerprints | yq -P`
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.59 | jq .fingerprints | yq -P`
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.13 | jq .fingerprints | yq -P`
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
-   hash: +7jdqCDr3gSvxYGgmyoxUiZo1Q8I1z7EVn75rkLVCZo
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f0:8f:6c:d6:de:59:ca:ac:6b:f0:7d:6c:5d:68:9c:f6
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
-   hash: z5usqZ3xMiWTM/+gaS3eK8eg4GDJ2pU3gdbftaOew3s
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 26:a9:d7:ee:ab:ec:96:90:68:77:7a:68:72:b0:94:76
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.36 | jq .fingerprints | yq -P`
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
-   hash: KjRYasXHzJNtqZcFUEvg1Ky1MPLf1XBo3vKT/aL+oQ0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0f:6a:ae:09:cb:16:f9:bb:4e:bd:d8:ed:a0:b6:5d:6f
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
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.54 | jq .fingerprints | yq -P`
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
## controller.webarch.net
SSH server fingerprints for `controller.webarch.net` at `81.95.52.35`:
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
## storage.webarchitects.coop
SSH server fingerprints for `storage.webarchitects.coop` at `81.95.52.125`:
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
<!-- BEGIN 81.95.52.7 -->
## unbound.webarch.org.uk
SSH server fingerprints for `unbound.webarch.org.uk` at `81.95.52.7`:
```yml
-   hash: mDaKZExz0P9PZUZdDjEUDJH/8K4frCsnnI1kh/glltQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c1:72:99:79:04:d4:35:09:c1:d8:0c:1f:4f:c0:e3:c7
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: P6ifPlN9owKZgV32l3glMYBu47kOe1XxVOfJx7B/+6k
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: f8:5a:a5:cb:0e:2a:10:1e:e3:a0:55:78:a5:f3:f1:68
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.7 | jq .fingerprints | yq -P`
<!-- END 81.95.52.7 -->
<!-- BEGIN 81.95.52.45 -->
## authentik.webarch.org.uk
SSH server fingerprints for `authentik.webarch.org.uk` at `81.95.52.45`:
```yml
-   hash: GfcSwVFn1d39BEhKnRgHf7ArKR8uEtyGgdrTfSaT1bQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 0f:52:0b:c6:dc:29:a8:df:87:cb:e3:91:a2:2a:ef:68
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 7nrCfc63X6DAo3OAyvpPnufkzx7BVlnD+J+9T9wVmFk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: b3:f7:cd:3b:a8:3d:cc:78:79:38:65:69:a9:0d:63:36
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
-   hash: ZSK26Rvwh4E5yyRxqf4fQkRKHhMXvwfjE4a9HmRcJoA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 80:25:46:78:16:24:a8:b2:dd:84:aa:ae:c6:d9:bd:f6
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 94.199.30.35 | jq .fingerprints | yq -P`
<!-- END 94.199.30.35 -->
<!-- BEGIN 81.95.52.16 -->
## plane.webarch.coop
SSH server fingerprints for `plane.webarch.coop` at `81.95.52.16`:
```yml
-   hash: eK6FUkfWnVTRyx+KIhy9XH/9DgexfMyZIzuDSEkYTPA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: db:34:e7:9f:4d:06:10:42:e3:d6:88:c8:ae:44:01:5a
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: UhnoEEu28jwme392aHi0+8aJhIGi4pAL3eJaeszDqFc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 36:c8:5f:12:84:a9:f5:45:7b:90:f0:24:b3:19:24:3f
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.16 | jq .fingerprints | yq -P`
<!-- END 81.95.52.16 -->
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
-   hash: p4VynOypbpYE/z7ngqscFQQxTVusgVIbe8VlZw4ZcdY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: e0:c7:6e:d2:d9:56:0e:b1:12:06:0a:ee:a9:32:7e:3c
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: XeUTRRuEwpneuurNR79mVy0J4O29hxBIjjWpEoS6KIc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 22:8d:ac:32:5c:be:5f:4e:a9:62:3d:12:b9:19:52:9c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.75 | jq .fingerprints | yq -P`
<!-- END 81.95.52.75 -->
<!-- BEGIN 81.95.52.123 -->
## green.webarch.net
SSH server fingerprints for `green.webarch.net` at `81.95.52.123`:
```yml
-   hash: MI4PPjyhCIhAu5XAF06gLbtCQBAqMCrIDxgrLHA9U2M
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b6:d6:22:72:ac:5c:63:c1:74:6c:2d:9d:a5:30:b0:6e
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: O383vVs7R9RDwPGw2a7T6HG01tm49i94lxwKf59Jeow
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 8b:d3:c2:63:89:cf:16:af:c4:ea:8d:58:e2:66:bb:b3
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.123 | jq .fingerprints | yq -P`
<!-- END 81.95.52.123 -->
<!-- BEGIN 81.95.52.23 -->
## mailman-1.webarchitects.coop
SSH server fingerprints for `mailman-1.webarchitects.coop` at `81.95.52.23`:
```yml
-   hash: hNc8JN0drq9v/8cV86ZOFMxIU+yuVa4jHuNQMOxfQHo
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: bc:8b:56:6e:26:41:b6:f6:d7:f6:ee:ab:b3:37:01:dd
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: DGw3gBxMSuK1PQyGXQceQ9eJOzh5sX0vIQWyCMqdccI
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 22:2b:fa:60:bc:5e:7f:74:4c:f0:b6:98:7a:17:7d:4b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.23 | jq .fingerprints | yq -P`
<!-- END 81.95.52.23 -->
<!-- BEGIN localhost -->
## workspace.webarch.org.uk
SSH server fingerprints for `workspace.webarch.org.uk` at `localhost`:
```yml
-   hash: p4VynOypbpYE/z7ngqscFQQxTVusgVIbe8VlZw4ZcdY
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: e0:c7:6e:d2:d9:56:0e:b1:12:06:0a:ee:a9:32:7e:3c
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: XeUTRRuEwpneuurNR79mVy0J4O29hxBIjjWpEoS6KIc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 22:8d:ac:32:5c:be:5f:4e:a9:62:3d:12:b9:19:52:9c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j localhost | jq .fingerprints | yq -P`
<!-- END localhost -->
<!-- BEGIN 81.95.52.66 -->
## mailcoopuk.webarch.net
SSH server fingerprints for `mailcoopuk.webarch.net` at `81.95.52.66`:
```yml
-   hash: x0iuarIzc90rWnr2P/SCt3EjNObzrdkHl/P8624e89k
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 58:62:ce:be:69:ff:06:fd:1f:cb:48:02:ad:24:0b:c4
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: C03YEz4jJu894ptewgR+tfEoUrTw6pEcamF9bwxb4ZU
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 0b:1f:f3:3d:7d:b8:d9:f9:de:d6:5b:14:76:ee:01:e7
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.66 | jq .fingerprints | yq -P`
<!-- END 81.95.52.66 -->
<!-- BEGIN 81.95.52.41 -->
## munin.webarch.org.uk
SSH server fingerprints for `munin.webarch.org.uk` at `81.95.52.41`:
```yml
-   hash: 0VfaZP7Hgy/vuvg9VYx5zTZtnC5GMPnWAkyy4MSDRW4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 81:d1:7d:a4:96:ef:e4:61:19:89:9a:6a:42:9c:0f:17
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: v+fqngzp9ArB2avmVjAhmn7pVerdta1NyGNGayN8Jfw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 68:35:08:da:2a:92:15:25:e2:0d:91:45:68:84:57:10
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.41 | jq .fingerprints | yq -P`
<!-- END 81.95.52.41 -->
<!-- BEGIN 81.95.52.44 -->
## odmworkspace.webarch.net
SSH server fingerprints for `odmworkspace.webarch.net` at `81.95.52.44`:
```yml
-   hash: BRh1Z+DknneAoBawtM9Dntmj3YHyHOb4ki1jqznQFyw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: c2:c5:21:46:ae:63:8a:31:4b:2a:b1:46:25:77:e9:ab
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: 9iCmi3MJNWR5n3RO7GmnZiw7Roi3Vgb0vJ6X75ArGQg
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 6d:5e:ec:a4:9e:bb:61:4f:aa:d1:a5:84:b0:55:20:99
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.44 | jq .fingerprints | yq -P`
<!-- END 81.95.52.44 -->
<!-- BEGIN 81.95.52.25 -->
## labourstart.webarchitects.co.uk
SSH server fingerprints for `labourstart.webarchitects.co.uk` at `81.95.52.25`:
```yml
-   hash: yHSAv4iOvO6KKG9rZNfXtKJ2+4z3AGfybgoG4uqX9h4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: a3:30:bd:d5:fc:dc:e4:06:09:a3:53:01:be:cc:96:d0
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: Np48O4rRtnWfIMIjk2vOvWnmb1w0zXHRwPBwitufskA
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5b:78:0b:6e:3c:d9:f7:21:4a:2e:da:95:6c:64:7c:28
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.25 | jq .fingerprints | yq -P`
<!-- END 81.95.52.25 -->
<!-- BEGIN 81.95.52.28 -->
## webarch8.co.uk
SSH server fingerprints for `webarch8.co.uk` at `81.95.52.28`:
```yml
-   hash: wz7V06VAxNu08QywRSTHMBqlN/LtgZzfRY/sUH8aH1o
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: d7:79:f9:e9:84:52:af:20:1b:61:96:55:b7:1b:6e:67
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: mBHyB4dg1VZh/A6tI6Ok/3w3RIC89cymJtf5x+BEO88
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 78:b1:cf:49:7d:4c:be:5d:6f:06:95:51:83:f6:9e:3c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.28 | jq .fingerprints | yq -P`
<!-- END 81.95.52.28 -->
<!-- BEGIN 81.95.52.10 -->
## unbound1.webarch.net
SSH server fingerprints for `unbound1.webarch.net` at `81.95.52.10`:
```yml
-   hash: QzBvEXrv+z9+ccLFdx6v2HzUSgd2Cvvk+avxSkh8xlE
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 72:ad:75:0c:b7:19:db:7b:0c:d0:36:90:95:59:05:2f
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: dfHj3ENKpmnar8MSmBqpPYekxjrrgno7sCrDXLUc8dk
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 77:dc:7a:2f:e8:aa:5e:b7:fb:50:fe:22:da:d9:cc:1b
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.10 | jq .fingerprints | yq -P`
<!-- END 81.95.52.10 -->
<!-- BEGIN 81.95.52.53 -->
## unbound2.webarch.net
SSH server fingerprints for `unbound2.webarch.net` at `81.95.52.53`:
```yml
-   hash: vfx+Ifud2blua6YDF0vnSNhQegzzQlTBQZtUpdgaXOw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 94:ae:72:9d:6a:5c:f8:58:27:a4:2c:ef:cf:5c:31:96
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: ZZJ5fNqNEc/WgEuZhJA7KdbKmmEnqLl/uA3xVWWihH0
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: c3:f3:bb:66:b4:24:88:77:ea:bf:ba:7c:21:d3:78:e5
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.53 | jq .fingerprints | yq -P`
<!-- END 81.95.52.53 -->
<!-- BEGIN 81.95.52.126 -->
## xen5.webarch.net
SSH server fingerprints for `xen5.webarch.net` at `81.95.52.126`:
```yml
-   hash: +FOyLYhSz8hzJuBuZr6XPCyzvkDVWr3P1mzHH6xK6Gw
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 1f:d2:19:13:be:40:9a:82:34:7b:33:96:7c:99:3c:bb
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: j2aUVfcgpQ5PKbL5+AYXqQBGRY/VVUxkloAZHb8OXbc
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 97:37:30:1b:8e:c7:a4:b4:3d:96:37:ef:55:37:02:36
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.126 | jq .fingerprints | yq -P`
<!-- END 81.95.52.126 -->
<!-- BEGIN 81.95.52.89 -->
## webmin.webarch.org.uk
SSH server fingerprints for `webmin.webarch.org.uk` at `81.95.52.89`:
```yml
-   hash: kGh5CZ/paQ5a/LfaqdoZT00qtCa8qQsNcEuEW1Yu8T4
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: 84:b7:d9:f9:9a:7a:4c:0b:1a:23:c5:be:f2:64:0b:47
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: vvigA0qtCJTsqIGBL5WnNUubu4w0Dxo2kOJoXWz9mN8
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bd:d9:5c:a9:cf:c1:fe:7c:4e:1a:1a:6f:fd:8e:67:78
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.89 | jq .fingerprints | yq -P`
<!-- END 81.95.52.89 -->
<!-- BEGIN 81.95.52.27 -->
## dns5.webarch.org.uk
SSH server fingerprints for `dns5.webarch.org.uk` at `81.95.52.27`:
```yml
-   hash: CmgekJv3veBqFfVt1TPCdk03lTFkAPxxuoAUwEo5ENU
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: dc:a8:67:1e:c1:64:ab:a9:db:9b:06:20:ea:ee:df:aa
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: IurSECKylKXp+ulFYARDW6EIdAfbPVNawGDHFbfeQJw
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 33:d3:08:06:c4:da:cd:58:b9:0a:11:c5:fd:59:fe:e0
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.27 | jq .fingerprints | yq -P`
<!-- END 81.95.52.27 -->
<!-- BEGIN 81.95.52.119 -->
## backup-b.webarch.net
SSH server fingerprints for `backup-b.webarch.net` at `81.95.52.119`:
```yml
-   hash: nBlVdhTw70Vx3Eku8LCZnRUaoCtUacY9yhIjJxtl7NA
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: b7:6b:5e:8d:7b:9b:69:52:f8:da:7e:09:96:e9:ad:84
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: FfNB4c4G4FDq/sBavYoNGSYbxA4H2ZU8CLxawdU5a1c
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: 5f:29:e3:79:7a:ae:27:c8:b1:fe:6d:e8:00:a7:bd:5c
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit -j 81.95.52.119 | jq .fingerprints | yq -P`
<!-- END 81.95.52.119 -->
<!-- BEGIN 81.95.52.24 -->
## dns0.webarchitects.co.uk
SSH server fingerprints for `dns0.webarchitects.co.uk` at `81.95.52.24`:
```yml
-   hash: SY1oVlMPi7uwpsQPesG/AZj3XL+rxo5wX3ZQWTFpCrQ
    hash_alg: SHA256
    hostkey: ssh-ed25519
-   hash: df:e6:04:ff:56:2e:8f:80:5f:7b:7e:a5:04:99:7e:e4
    hash_alg: MD5
    hostkey: ssh-ed25519
-   hash: Ld0cnf4sAGv6kNkeelZVHfBhWgMdQgknI8OiPKw24FQ
    hash_alg: SHA256
    hostkey: ssh-rsa
-   hash: bc:22:c8:7c:45:0d:56:03:b4:2a:ae:c5:1a:d2:66:fb
    hash_alg: MD5
    hostkey: ssh-rsa

```
The above YAML can generated using `ssh-audit --skip-rate-test -j 81.95.52.24 | jq .fingerprints | yq -P`
<!-- END 81.95.52.24 -->

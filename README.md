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
Include ~/.ssh/webarch-ssh/*.host
```

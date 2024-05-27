# About

Personal [Portage Overlay](https://wiki.gentoo.org/wiki/Project:Overlays) for [Gentoo](https://www.gentoo.org) Linux based systems.

## Note

Currently, it's a boilerplate repository.

## Using This Repository

There are many ways to use this repository. The following are two methods:

### Local Repository

For the [local repository](https://wiki.gentoo.org/wiki/Handbook:Parts/Portage/CustomTree#Defining_a_custom_repository) method, create a `/etc/portage/repos.conf/tanvir` file and add the following:

```r
[tanvir]
priority = 10
location = /var/db/repos/tanvir
sync-type = git
sync-uri = git://github.com/tanvir/portage-overlay.git
auto-sync = Yes
```

Then run `<superuser> emerge --sync tanvir`. Portage should now find and update the repository.

### Layman

You can also use the Layman tool to add and sync the repository. Execute the following:

```sh
<superuser> layman -o https://raw.githubusercontent.com/tanvir/portage-overlay/dev/repository.xml -f -a tanvir
```

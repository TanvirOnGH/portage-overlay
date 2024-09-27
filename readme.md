# About

Personal [Portage Overlay](https://wiki.gentoo.org/wiki/Project:Overlays) for [Gentoo](https://www.gentoo.org) Linux based systems.

> [!NOTE]  
> Currently, it's a boilerplate repository.

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

### Eselect

You can also use the [eselect repository](https://wiki.gentoo.org/wiki/Eselect/Repository) method. Execute the following:

```sh
<superuser> eselect repository add tanvir git "https://gitlab.com/tanvir/portage-overlay"
```

Or, simply from the official list: `<superuser> eselect repository enable tanvir`.

### Layman

You can also use the Layman tool to add and sync the repository. Execute the following:

```sh
<superuser> layman -o https://raw.githubusercontent.com/tanvir/portage-overlay/dev/repository.xml -f -a tanvir
```

Or, simply from the official list: `<superuser> layman -a tanvir`.

### Zugaina

Find my packages/overlay at: [gpo.zugaina.org/Overlays/tanvir](https://gpo.zugaina.org/Overlays/tanvir)

## References

- [Gentoo Linux](https://www.gentoo.org)
- [Portage](https://wiki.gentoo.org/wiki/Portage)
- [Gentoo Overlays](https://wiki.gentoo.org/wiki/Project:Overlays)
- [Zugaina - Gentoo Portage Overlays](https://gpo.zugaina.org)

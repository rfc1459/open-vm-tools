open-vm-tools overlay
---------------------

This Portage overlay is a fork of the [fol4][] overlay containing only
up-to-date ebuilds for open-vm-tools.

### Installation

Save the following file as `/etc/layman/overlays/open-vm-tools.xml`:

```xml
<repositories version="1.0">
  <repo quality="experimental" status="unofficial">
    <name>open-vm-tools</name>
    <description lang="en">Unofficial ebuilds for open-vm-tools</description>
    <homepage>https://github.com/rfc1459/open-vm-tools</homepage>
    <owner type="person">
      <email>morpheus@level28.org</email>
      <name>Matteo Panella</name>
    </owner>
    <source type="git">git://github.com/rfc1459/open-vm-tools.git</source>
  </repo>
</repositories>
```

Then use [layman][] to activate the repository.

I urge you to hard-mask `*/*::open-vm-tools` and unmask single packages
as-needed. I plan to keep only packages related to open-vm-tools here, but
hard-masking overlays is currently considered best practice (that is, unless
you're the overlay owner).


[fol4]: https://github.com/madsl/fol4
[layman]: http://wiki.gentoo.org/wiki/Layman

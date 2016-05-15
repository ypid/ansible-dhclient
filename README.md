## dhclient

<!-- This file was generated by Ansigenome. Do not edit this file directly but
     instead have a look at the files in the ./meta/ directory. -->

[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](#)
[![GitHub Tags](https://img.shields.io/github/tag/ypid/ansible-dhclient.svg)](https://github.com/ypid/ansible-dhclient)
[![GitHub Stars](https://img.shields.io/github/stars/ypid/ansible-dhclient.svg)](https://github.com/ypid/ansible-dhclient)

Configure dhclient.

Configure the hostname to be send by `dhclient` in case it should differ
from the system hostname.



### Role variables

List of default variables available in the inventory:

```YAML
---
# Default variables
# =================

# .. contents:: Sections
#    :local:
#
# .. Required packages (((
#
# ---------------------
#   Required packages
# ---------------------

# .. envvar:: dhclient__base_packages
#
# List of base packages to install.
dhclient__base_packages:
  - 'isc-dhcp-client'

# .. )))

# .. dhclient configuration (((
#
# --------------------------
#   dhclient configuration
# --------------------------

# .. envvar:: dhclient__send_hostname
#
# Hostname to send by ``dhclient``. When an ``gethostname()`` is defined, the
# hostname will not be explicitly set in :file:`/etc/dhcp/dhclient.conf` which
# should result in the system hostname being used.
dhclient__send_hostname: 'gethostname()'

# .. )))
```




### Authors and license

`dhclient` role was written by:

- [Robin Schneider](http://ypid.de/) | [e-mail](mailto:ypid@riseup.net) | [Twitter](https://twitter.com/ypid) | [GitHub](https://github.com/ypid)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).

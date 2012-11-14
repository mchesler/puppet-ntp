# NTP Module

Matt Chesler <mchesler@chesent.com>

This module manages NTP via Puppet

# Quick Start

Install and configure NTP

```
node default: {
  class { 'ntp': }
}
```

# Sample Usage

Configure NTP client with non-standard servers/options
```
class {'ntp':
  servers => [ "ntp1.example.com dynamic",
               "ntp2.example.com dynamic", ],
}
```

Explicitly disable NTP (on a virtual machine for example)
```
class {'ntp':
  enable => false,
  ensure => stopped,
}
```

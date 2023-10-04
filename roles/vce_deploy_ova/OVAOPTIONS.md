# deploymentOption
| Parameter | Default | Label | vCPU | Memory | Disk | Hosts | VMs |
|---|---|---|---|---|---|---|---|
| small-light | | Small Light vCenter Server with Embedded PSC - for VMC consumption, unsupported for on-prem customers | 4 vCPU | 19 GB | 494 GB | 100 Hosts | 1000 VMs |
| medium-light | | Medium Light vCenter Server with Embedded PSC - for VMC consumption, unsupported for on-prem customers | 8 vCPU | 28 GB | 708 GB | 400 Hosts | 4000 VMs |
| large-light | | Large Light vCenter Server with Embedded PSC - for VMC consumption, unsupported for on-prem customers | 16 vCPU | 37 GB | 1058 GB | 1000 Hosts | 10000 VMs |
| tiny | * | Tiny vCenter Server with Embedded PSC | 2 vCPU | 14 GB | 579 GB | 10 Hosts | 100 VMs |
| small | | Small vCenter Server with Embedded PSC | 4 vCPU | 21 GB | 694 GB | 100 Hosts | 1000 VMs |
| medium | | Medium vCenter Server with Embedded PSC | 8 vCPU | 30 GB | 908 GB | 400 Hosts | 4000 VMs |
| large | | Large vCenter Server with Embedded PSC | 16 vCPU | 39 GB | 1358 GB | 1000 Hosts | 10000 VMs |
| xlarge | | X-Large vCenter Server with Embedded PSC | 24 vCPU | 58 GB | 2283 GB | 2000 Hosts | 35000 VMs |
| tiny-lstorage | | Tiny vCenter Server with Embedded PSC (large storage) | 2 vCPU | 14 GB | 2019 GB | 10 Hosts | 100 VMs |
| small-lstorage | | Small vCenter Server with Embedded PSC (large storage) | 4 vCPU | 21 GB | 2044 GB | 100 Hosts | 1000 VMs |
| medium-lstorage | | Mediun vCenter Server with Embedded PSC (large storage) | 8 vCPU | 30 GB | 2208 GB | 400 Hosts | 4000 VMs |
| large-lstorage | | Large vCenter Server with Embedded PSC (large storage) | 16 vCPU | 39 GB | 2258 GB | 1000 Hosts | 10000 VMs |
| xlarge-lstorage | | X-Large vCenter Server with Embedded PSC (large storage) | 24 vCPU | 58 GB | 2383 GB | 2000 Hosts | 35000 VMs |
| tiny-xlstorage | | Tiny vCenter Server with Embedded PSC (x-large storage) | 2 vCPU | 14 GB | 4279 GB | 10 Hosts | 100 VMs |
| small-xlstorage | | Small vCenter Server with Embedded PSC (x-large storage) | 4 vCPU | 21 GB | 4304 GB | 100 Hosts | 1000 VMs |
| medium-xlstorage | | Medium vCenter Server with Embedded PSC (x-large storage) | 8 vCPU | 30 GB | 4468 GB | 400 Hosts | 4000 VMs |
| large-xlstorage | | Large vCenter Server with Embedded PSC (x-large storage) | 16 vCPU | 39 GB | 4518 GB | 1000 Hosts | 10000 VMs |
| xlarge-xlstorage | | X-Large vCenter Server with Embedded PSC (x-large storage) | 24 vCPU | 58 GB | 4643 GB | 2000 Hosts | 35000 VMs |

# Application
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|

| Network Configuration ||
| guestinfo.cis.appliance.net.addr.family | true | | Host Network IP Address Family | Network IP address family (i.e., &apos;ipv4&apos; or &apos;ipv6&apos;). |
| guestinfo.cis.appliance.net.mode | true | | Host Network Mode | Network mode (i.e., &apos;static&apos;, &apos;dhcp&apos;, or &apos;autoconf&apos; (IPv6 only). |
| guestinfo.cis.appliance.net.addr | true | | Host Network IP Address | Network IP address.  Only provide this when mode is &apos;static&apos;.  Can be IPv4 or IPv6 based on specified address family. |
| guestinfo.cis.appliance.net.prefix | true | | Host Network Prefix | Network prefix length.  Only provide this when mode is &apos;static&apos;.  0-32 for IPv4.  0-128 for IPv6. |
| guestinfo.cis.appliance.net.gateway | true | | Host Network Default Gateway | IP address of default gateway.  Can be &apos;default&apos; when using IPv6. |
| guestinfo.cis.appliance.net.dns.servers | true | | Host Network DNS Servers | Comma separated list of IP addresses of DNS servers. |
| guestinfo.cis.appliance.net.pnid | true | | Host Network Identity | Network identity (IP address or fully-qualified domain name) services should use when advertising themselves. |
| guestinfo.cis.appliance.net.ports | false | {} | Custom Network Ports | A string encoding a JSON object mapping port names to port numbers. |

| SSO Configuration||
| guestinfo.cis.vmdir.username | false | administrator@vsphere.local | Directory Username | For the first instance of the identity domain, this is the username with Administrator privileges. Otherwise, this is the username of the replication partner. |
| guestinfo.cis.vmdir.password | true | | Directory Password | For the first instance of the identity domain, this is the password given to the Administrator account.  Otherwise, this is the password of the Administrator account of the replication partner. |
| guestinfo.cis.vmdir.domain-name | false | vsphere.local | Directory Domain Name | For the first instance of the identity domain, this is the name of the newly created domain |
| guestinfo.cis.vmdir.site-name | false | Default-First-Site | Site Name | Name of site.  Use &apos;Default-First-Site&apos; to define a new site. |
| guestinfo.cis.vmdir.first-instance | false | True | New Identity Domain | If this parameter is set to True, the VMware directory instance is setup as the first instance of a new identity domain. Otherwise, the instance is setup as a replication partner. |
| guestinfo.cis.vmdir.replication-partner-hostname | false | "" | Directory Replication Partner | The hostname of the VMware directory replication partner.  This value is ignored for the first instance of the identity domain. |

| Database Configuration ||
| guestinfo.cis.db.type | false | embedded | Database Type | String indicating whether the database is &apos;embedded&apos; or &apos;external&apos;. |
| guestinfo.cis.db.user | false | "" | Database User | String naming the account to use when connecting to external database (ignored when db.type is &apos;embedded&apos;). |
| guestinfo.cis.db.password | false | "" | Database Password | String providing the password to use when connecting to external database (ignored when db.type is &apos;embedded&apos;). |
| guestinfo.cis.db.servername | false | "" | Database Server | String naming the hostname of the server on which the external database is running (ignored when db.type is &apos;embedded&apos;). |
| guestinfo.cis.db.serverport | false | "" | Database Port | String describing the port on the host on which the external database is running (ignored when db.type is &apos;embedded&apos;). |
| guestinfo.cis.db.provider | false | "" | Database Provider | String describing the external database provider. The only supported value is &apos;oracle&apos; (ignored when the db.type is &apos;embedded&apos;). |
| guestinfo.cis.db.instance | false | "" | Database Instance | String describing the external database instance. Values could be anything depending on what the database instance name the DBA creates in the external db. (ignored when the db.type is &apos;embedded&apos;). |

| System Configuration ||
| guestinfo.cis.appliance.root.passwd | true |  | Root Password | Password to assign to root account.  If blank, password can be set on the console. |
| guestinfo.cis.appliance.root.shell | false | "" | Root Shell | This property is not changeable. |
| guestinfo.cis.appliance.ssh.enabled | false | False | SSH Enabled | Set whether SSH-based remote login is enabled.  This configuration can be changed after deployment. |
| guestinfo.cis.appliance.time.tools-sync | false | False | Tools-based Time Synchronization Enabled | Set whether VMware tools based time synchronization should be used. This parameter is ignored if appliance.ntp.servers is not empty. |
| guestinfo.cis.appliance.ntp.servers | false | "" | NTP Servers | A comma-separated list of hostnames or IP addresses of NTP Servers |
| guestinfo.cis.deployment.node.type | false | embedded | Deployment Type | Type of appliance to deploy (i.e. &apos;embedded&apos;). |
| guestinfo.cis.system.vm0.hostname | false | "" | Platform Services Controller | When deploying a vCenter Server Node, please provide the FQDN or IP address of a Platform Services Controller (leave blank otherwise).  The choice of FQDN versus IP address is decided based on the Platform Services Controller&apos;s own notion of its network identity. |
| guestinfo.cis.system.vm0.port | false | 443 | HTTPS Port on Platform Services Controller | When deploying a vCenter Server pointing to an external platform services controller, please provide the HTTPS port of the external platform services controller if a custom port number is being used. The default HTTPS port number is 443. |

| Upgrade Configuration ||
| guestinfo.cis.upgrade.source.vpxd.ip | false | "" | Upgrade Source Hostname | IP/hostname of the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.ma.port | false | 9123 | Migration Assistant Port | Port used by Migration Assistant on source vCenter Server. |
| guestinfo.cis.upgrade.source.vpxd.user | false | "" | Upgrade Source vCenter Username | vCenter username for the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.vpxd.password | false | "" | Upgrade Source vCenter Password | vCenter password for the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guest.user | false | "" | Upgrade Source OS Username | Username for the appliance operating system to upgrade.  Usually root. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guest.password | false | "" | Upgrade Source OS Password | Password for the appliance operating system to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.addr | false | "" | Upgrade Management Host Hostname | URL that consists of the IP address or FQDN and https port of the vCenter Server instance or ESXi host that manages the appliance to upgrade. Https port is an optional parameter which by default is 443. Example: 10.10.10.10, //10.10.10.10:444, //[2001:db8:a0b:12f0::1]:444. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.user | false | "" | Upgrade Management Host Username | Username for the host that manages appliance to upgrade.  Can be  either vCenter or ESX host.  Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.password | false | "" | Upgrade Management Host Password | Password for the host that manages appliance to upgrade.  Can be  either vCenter or ESX host.  Set only for upgrade. |
| guestinfo.cis.upgrade.source.ssl.thumbprint | false | "" | xxx | xxx |
| guestinfo.cis.upgrade.source.platform | false | linux | xxx | xxx |
| guestinfo.cis.upgrade.source.export.directory | false | /var/tmp | xxx | xxx |
| guestinfo.cis.upgrade.import.directory | xxx | xxx | xxx | xxx |
| guestinfo.cis.upgrade.user.options | xxx | xxx | xxx | xxx |
| guestinfo.cis.ad.domain-name | xxx | xxx | xxx | xxx |
| guestinfo.cis.ad.domain.username | xxx | xxx | xxx | xxx |
| guestinfo.cis.ad.domain.password | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.management.addr | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.management.port | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.management.user | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.management.password | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.management.thumbprint | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.ha.placement | xxx | xxx | xxx | xxx |

| Miscellaneous ||
| guestinfo.cis.netdump.enabled | xxx | xxx | xxx | xxx |
| guestinfo.cis.silentinstall | xxx | xxx | xxx | xxx |
| guestinfo.cis.lookup_timeout | xxx | xxx | xxx | xxx |
| guestinfo.cis.clientlocale | xxx | xxx | xxx | xxx |
| guestinfo.cis.feature.states | xxx | xxx | xxx | xxx |
| guestinfo.cis.ceip_enabled | xxx | xxx | xxx | xxx |
| guestinfo.cis.deployment.autoconfig | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.mac-allocation-scheme.prefix | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.mac-allocation-scheme.prefix-length | xxx | xxx | xxx | xxx |
| guestinfo.cis.vpxd.mac-allocation-scheme.ranges | xxx | xxx | xxx | xxx |
| guestinfo.cis.plugin-isolation.hostname | xxx | xxx | xxx | xxx |
| guestinfo.cis.osgi.settings.isolation | xxx | xxx | xxx | xxx |
| guestinfo.cis.hadcs.enabled | xxx | xxx | xxx | xxx |
| guestinfo.cis.fips.enabled | xxx | xxx | xxx | xxx |
| guestinfo.cis.desired.state | xxx | xxx | xxx | xxx |
| guestinfo.cis.vsan.postfirstboot.setting | xxx | xxx | xxx | xxx |
| guestinfo.cis.env.classification.level | xxx | xxx | xxx | xxx |
| guestinfo.cis.vc.desired.state | xxx | xxx | xxx | xxx |
| guestinfo.cis.deployment.license | xxx | xxx | xxx | xxx |

# VAMI Properties
## Networking Properties
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| domain | true | | Domain Name | The domain name of this VM. Leave blank if DHCP is desired. |
| searchpath | true | | Domain Search Path | The domain search path (comma or space separated domain names) for this VM. Leave blank if DHCP is desired. |

# VM specific properties
| vmname | | VMware-vCenter-Server-Appliance | | |

# Network
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| Network 1 | | | | The "Network 1" network |
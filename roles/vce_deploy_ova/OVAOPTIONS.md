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

# VAMI Properties
## Networking Properties
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| vami.domain.VMware-vCenter-Server-Appliance | true | | Domain Name | The domain name of this VM. Leave blank if DHCP is desired. |
| vami.searchpath.VMware-vCenter-Server-Appliance | true | | Domain Search Path | The domain search path (comma or space separated domain names) for this VM. Leave blank if DHCP is desired. |

## VM specific properties
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| vm.vmname | | VMware-vCenter-Server-Appliance | | |

## Network
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| Network 1 | | | | The "Network 1" network |

# Application
## Network Configuration
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.appliance.net.addr.family | true | | Host Network IP Address Family | Network IP address family (i.e., 'ipv4' or 'ipv6'). |
| guestinfo.cis.appliance.net.mode | true | | Host Network Mode | Network mode (i.e., 'static', 'dhcp', or 'autoconf' (IPv6 only). |
| guestinfo.cis.appliance.net.addr | true | | Host Network IP Address | Network IP address.  Only provide this when mode is 'static'.  Can be IPv4 or IPv6 based on specified address family. |
| guestinfo.cis.appliance.net.prefix | true | | Host Network Prefix | Network prefix length.  Only provide this when mode is 'static'.  0-32 for IPv4.  0-128 for IPv6. |
| guestinfo.cis.appliance.net.gateway | true | | Host Network Default Gateway | IP address of default gateway.  Can be 'default' when using IPv6. |
| guestinfo.cis.appliance.net.dns.servers | true | | Host Network DNS Servers | Comma separated list of IP addresses of DNS servers. |
| guestinfo.cis.appliance.net.pnid | true | | Host Network Identity | Network identity (IP address or fully-qualified domain name) services should use when advertising themselves. |
| guestinfo.cis.appliance.net.ports | false | {} | Custom Network Ports | A string encoding a JSON object mapping port names to port numbers. |

## SSO Configuration
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.vmdir.username | false | administrator@vsphere.local | Directory Username | For the first instance of the identity domain, this is the username with Administrator privileges. Otherwise, this is the username of the replication partner. |
| guestinfo.cis.vmdir.password | true | | Directory Password | For the first instance of the identity domain, this is the password given to the Administrator account.  Otherwise, this is the password of the Administrator account of the replication partner. |
| guestinfo.cis.vmdir.domain-name | false | vsphere.local | Directory Domain Name | For the first instance of the identity domain, this is the name of the newly created domain |
| guestinfo.cis.vmdir.site-name | false | Default-First-Site | Site Name | Name of site.  Use 'Default-First-Site' to define a new site. |
| guestinfo.cis.vmdir.first-instance | false | True | New Identity Domain | If this parameter is set to True, the VMware directory instance is setup as the first instance of a new identity domain. Otherwise, the instance is setup as a replication partner. |
| guestinfo.cis.vmdir.replication-partner-hostname | false | "" | Directory Replication Partner | The hostname of the VMware directory replication partner.  This value is ignored for the first instance of the identity domain. |

## Database Configuration
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.db.type | false | embedded | Database Type | String indicating whether the database is 'embedded' or 'external'. |
| guestinfo.cis.db.user | false |"" | Database User | String naming the account to use when connecting to external database (ignored when db.type is 'embedded'). |
| guestinfo.cis.db.password | false |  | Database Password | String providing the password to use when connecting to external database (ignored when db.type is 'embedded'). |
| guestinfo.cis.db.servername | false |  | Database Server | String naming the hostname of the server on which the external database is running (ignored when db.type is 'embedded'). |
| guestinfo.cis.db.serverport | false |  | Database Port | String describing the port on the host on which the external database is running (ignored when db.type is 'embedded'). |
| guestinfo.cis.db.provider | false |  | Database Provider | String describing the external database provider. The only supported value is 'oracle' (ignored when the db.type is 'embedded'). |
| guestinfo.cis.db.instance | false |  | Database Instance | String describing the external database instance. Values could be anything depending on what the database instance name the DBA creates in the external db. (ignored when the db.type is 'embedded'). |

## System Configuration
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.appliance.root.passwd | true |  | Root Password | Password to assign to root account.  If blank, password can be set on the console. |
| guestinfo.cis.appliance.root.shell | false |  | Root Shell | This property is not changeable. |
| guestinfo.cis.appliance.ssh.enabled | false | False | SSH Enabled | Set whether SSH-based remote login is enabled.  This configuration can be changed after deployment. |
| guestinfo.cis.appliance.time.tools-sync | false | False | Tools-based Time Synchronization Enabled | Set whether VMware tools based time synchronization should be used. This parameter is ignored if appliance.ntp.servers is not empty. |
| guestinfo.cis.appliance.ntp.servers | false |  | NTP Servers | A comma-separated list of hostnames or IP addresses of NTP Servers |
| guestinfo.cis.deployment.node.type | false | embedded | Deployment Type | Type of appliance to deploy (i.e. 'embedded'). |
| guestinfo.cis.system.vm0.hostname | false |  | Platform Services Controller | When deploying a vCenter Server Node, please provide the FQDN or IP address of a Platform Services Controller (leave blank otherwise).  The choice of FQDN versus IP address is decided based on the Platform Services Controller's own notion of its network identity. |
| guestinfo.cis.system.vm0.port | false | 443 | HTTPS Port on Platform Services Controller | When deploying a vCenter Server pointing to an external platform services controller, please provide the HTTPS port of the external platform services controller if a custom port number is being used. The default HTTPS port number is 443. |

## Upgrade Configuration
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.upgrade.source.vpxd.ip | false |  | Upgrade Source Hostname | IP/hostname of the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.ma.port | false | 9123 | Migration Assistant Port | Port used by Migration Assistant on source vCenter Server. |
| guestinfo.cis.upgrade.source.vpxd.user | false |  | Upgrade Source vCenter Username | vCenter username for the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.vpxd.password | false |  | Upgrade Source vCenter Password | vCenter password for the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guest.user | false |  | Upgrade Source OS Username | Username for the appliance operating system to upgrade.  Usually root. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guest.password | false |  | Upgrade Source OS Password | Password for the appliance operating system to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.addr | false |  | Upgrade Management Host Hostname | URL that consists of the IP address or FQDN and https port of the vCenter Server instance or ESXi host that manages the appliance to upgrade. Https port is an optional parameter which by default is 443. Example: 10.10.10.10, //10.10.10.10:444, //[2001:db8:a0b:12f0::1]:444. Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.user | false |  | Upgrade Management Host Username | Username for the host that manages appliance to upgrade.  Can be  either vCenter or ESX host.  Set only for upgrade. |
| guestinfo.cis.upgrade.source.guestops.host.password | false |  | Upgrade Management Host Password | Password for the host that manages appliance to upgrade.  Can be  either vCenter or ESX host.  Set only for upgrade. |
| guestinfo.cis.upgrade.source.ssl.thumbprint | false |  | Upgrade Management Host Thumbprint | Thumbprint for the SSL certificate of the host that manages the appliance to upgrade. Set only for upgrade. |
| guestinfo.cis.upgrade.source.platform | false | linux | Upgrade Source Platform | Source host platform. Optional. Set only for upgrade |
| guestinfo.cis.upgrade.source.export.directory | false | /var/tmp | Upgrade Source Export Folder | Folder on the source appliance, where to store migrate data. Optional. Set only for upgrade |
| guestinfo.cis.upgrade.import.directory | false | /storage/seat/cis-export-folder | Upgrade Destination Export Folder | Folder where exported source data will be stored in the appliance. Optional. Set only for upgrade |
| guestinfo.cis.upgrade.user.options | false |  | Upgrade Advanced Options | Advanced upgrade settings specified in json format. Optional. Set only for upgrade |
| guestinfo.cis.ad.domain-name | false |  | Active Directory domain name | Active Directory domain to join. |
| guestinfo.cis.ad.domain.username | false |  | Active Directory domain admin user | Active Directory domain admin user. This username will be used to join the machine to the domain. |
| guestinfo.cis.ad.domain.password | false |  | Active Directory domain admin user password | Active Directory domain admin user password. This password will be used to join the machine to the domain. |
| guestinfo.cis.vpxd.ha.management.addr | true | | vCenter Server managing target appliance | FQDN or IP address of the vCenter Server managing that target appliance. Used when upgrading a source appliance in VCHA cluster. |
| guestinfo.cis.vpxd.ha.management.port | true | 443 | Port of the vCenter Server managing target appliance | Https port of the vCenter Server managing that target appliance. Used when upgrading a source appliance in VCHA cluster. If not specified, port 443 will be used by default. |
| guestinfo.cis.vpxd.ha.management.user | true | | Username for the vCenter Server managing target appliance | User able to authenticate in vCenter Server managing that target appliance. The user must have the privilege Global.VCServer. Used when upgrading a source appliance in VCHA cluster. |
| guestinfo.cis.vpxd.ha.management.password | true | | Password for the vCenter Server managing target appliance | Password for administrator user authenticating to the vCenter Server managing target appliance. Used when upgrading a source appliance in VCHA cluster. |
| guestinfo.cis.vpxd.ha.management.thumbprint | true | | Thumbprint for the SSL certificate of the vCenter Server managing target appliance | Thumbprint for the SSL certificate of the vCenter Server that manages the appliance to upgrade. Used when upgrading a source appliance in VCHA cluster. |
| guestinfo.cis.vpxd.ha.placement | true | | Path to the compute resource where target appliance will be deployed on management vCenter Server | Path to host/cluster/resource pool where target appliance will be deployed on management vCenter Server. Used when upgrading a source appliance in VCHA cluster. Example: /my_datacenter/my_folder/my_host_or_cluster/my_resource_pool |

## Miscellaneous
| Parameter | UserConfigurable | Default | Label | Description |
|---|---|---|---|---|
| guestinfo.cis.netdump.enabled | false | True | ESXi Dump Collector Enabled | Set whether ESXi Dump Collector service is enabled.  This configuration can be changed after deployment. |
| guestinfo.cis.silentinstall | false | False | Do Silent Install | If this parameter is set to True, no questions will be posted during install or upgrade. Otherwise, the install process will wait for a reply if there is a pending question. |
| guestinfo.cis.lookup_timeout | false | 900 | DNS reverse lookup timeout | This parameter provides time in seconds, to retry DNS reverse lookup. This is only needed for parallel installation of VCSA and NSX_T. |
| guestinfo.cis.clientlocale | false | en | The Client Locale | This parameter specifies the client locale. Supported locales are en, fr, ja, ko, zh_CN and zh_TW. English is assumed if locale is unknown. |
| guestinfo.cis.feature.states | false | | Feature switch states | Specify feature switch states which need to be added or modified in feature switch state config file. Format: key1=value1, key2=value2 |
| guestinfo.cis.ceip_enabled | true | False | CEIP enabled | VMware’s Customer Experience Improvement Program ("CEIP") provides VMware with information that enables VMware to improve its products and services, to fix problems, and to advise you on how best to deploy and use our products. As part of the CEIP, VMware collects technical information about your organization’s use of VMware products and services on a regular basis in association with your organization’s VMware license key(s). This information does not personally identify any individual. For more details about the Program and how VMware uses the information it collects through CEIP, please see the product documentation at http://www.vmware.com/info?id=1399. If you want to participate in VMware’s CEIP for this product, set this property to True. You may join or leave VMware’s CEIP for this product at any time. |
| guestinfo.cis.deployment.autoconfig | false | False | Auto Start Services | If this parameter is set to True, the appliance will be configured after deployment using the specified OVF configuration parameters. If set to False, the appliance should be configured post-deployment using the VMware Appliance Management Interface. |
| guestinfo.cis.vpxd.mac-allocation-scheme.prefix | false | | MAC address allocation scheme prefix | If a valid MAC address prefix is provided, then all MAC addresses assigned by vCenter Server will begin with this prefix instead of the VMware OUI. This property cannot co-exist with mac-allocation-scheme.ranges |
| guestinfo.cis.vpxd.mac-allocation-scheme.prefix-length | false | 0 | MAC address allocation scheme prefix length | This property is mandatory whenever a custom MAC prefix is provided. |
| guestinfo.cis.vpxd.mac-allocation-scheme.ranges | false | | MAC address allocation scheme ranges | If valid MAC address range is provided, then vCenter Server will assign MAC addresses from this range instead of allocating VMware OUI based MAC address. The address range must be provided in the format "BeginAddress1-EndAddress1,...,BeginAddressN-EndAddressN". This property cannot co-exist with mac-allocation-scheme.prefix. |
| guestinfo.cis.plugin-isolation.hostname | false | | Hostname to use when loading vSphere Client plugins in the browser. | Isolation hostname that guards plugins from interfering with the core vSphere UI. |
| guestinfo.cis.osgi.settings.isolation | false | | Local plugins for which to add an isolation exception in the vSphere Client. | Local plugins for which the vSphere Client will not apply isolation. Format: plugin1, plugin2, plugin3 |
| guestinfo.cis.hadcs.enabled | true | True | Control HADCS enablement | If this parameter is set to True, the HADCS functionality will be enabled on the vCenter inventory. If set to False, the HADCS functionality will be disabled on the vCenter inventory. |
| guestinfo.cis.fips.enabled | false | False | Control VC FIPS enablement | If this parameter is set to True, the vCenter will be started in FIPS compliant mode. If set to False, the vCenter will be started in non-FIPS compliant mode. |
| guestinfo.cis.desired.state | false | {} | Desired State Configuations | String encoding JSON object desired state configuration which will be acquired by the deployment. |
| guestinfo.cis.vsan.postfirstboot.setting | true | | VSAN post first boot settings | If this property is set, the vCenter will be installed on a new VSAN cluster containing the target host. dcname, dedupEnabled, clusterName, vsanLicenseKey, and firstHost properties should be set with this. For example: {'dcName':'vsanDC','clusterName':'vsanCluster','dedupEnabled':false,'vsanLicenseKey':'','firstHost':{'hostName':'10.109.45.3','port':443,'userName':'root','password':'ca$hc0w'}}. |
| guestinfo.cis.env.classification.level | false | none | IL6 classifciation level | Impact Level 6 classification level. Supported values: 'none', 'unclassified', 'controlled', 'cui', 'confidential', 'secret', 'topsecret', 'topsecret_sci'. |
| guestinfo.cis.vc.desired.state | false | {} | vCenter Desired State Configuations | String encoding JSON object desired state configuration which will be acquired by the deployment. |
| guestinfo.cis.deployment.license | false | | vCenter License | The licenses to apply during the deployment or upgrade. Format: name1=key1,name2=key2 |

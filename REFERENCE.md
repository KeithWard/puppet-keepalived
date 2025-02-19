# Reference

<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

### Classes

* [`keepalived`](#keepalived): Install and configure keepalived
* [`keepalived::config`](#keepalivedconfig): Configure keepalived module
* [`keepalived::global_defs`](#keepalivedglobal_defs): Manage keepalived notifictions
* [`keepalived::install`](#keepalivedinstall): Install keepalived package
* [`keepalived::service`](#keepalivedservice): Manage keepalived service

### Defined types

#### Public Defined types

* [`keepalived::lvs::real_server`](#keepalivedlvsreal_server): Add a real server to a Linux Virtual Server with keepalived
* [`keepalived::lvs::virtual_server`](#keepalivedlvsvirtual_server): Configure a Linux Virtual Server with keepalived

Work in progress, supports:
  - single IP/port virtual servers
  - TCP_CHECK healthchecks
* [`keepalived::vrrp::instance`](#keepalivedvrrpinstance): Configure VRRP instance
* [`keepalived::vrrp::script`](#keepalivedvrrpscript): Configure VRRP script
* [`keepalived::vrrp::sync_group`](#keepalivedvrrpsync_group): Configure the group for instance
* [`keepalived::vrrp::track_process`](#keepalivedvrrptrack_process): Configure the process tracker

#### Private Defined types

* `keepalived::vrrp::unicast_peer`: Define a unicast peer for a vrrp instance.

### Data types

* [`Keepalived::Options`](#keepalivedoptions): keepalived::options
* [`Keepalived::Vrrp::Instance::VRule`](#keepalivedvrrpinstancevrule): keepalived::vrrp::instance::vrule

## Classes

### <a name="keepalived"></a>`keepalived`

Install and configure keepalived

#### Parameters

The following parameters are available in the `keepalived` class:

* [`sysconf_dir`](#sysconf_dir)
* [`sysconf_options`](#sysconf_options)
* [`config_dir`](#config_dir)
* [`config_dir_mode`](#config_dir_mode)
* [`config_file_mode`](#config_file_mode)
* [`config_group`](#config_group)
* [`config_owner`](#config_owner)
* [`daemon_group`](#daemon_group)
* [`daemon_user`](#daemon_user)
* [`pkg_ensure`](#pkg_ensure)
* [`pkg_list`](#pkg_list)
* [`service_enable`](#service_enable)
* [`service_ensure`](#service_ensure)
* [`service_hasrestart`](#service_hasrestart)
* [`service_hasstatus`](#service_hasstatus)
* [`service_manage`](#service_manage)
* [`service_name`](#service_name)
* [`service_restart`](#service_restart)
* [`vrrp_instance`](#vrrp_instance)
* [`vrrp_script`](#vrrp_script)
* [`vrrp_track_process`](#vrrp_track_process)
* [`vrrp_sync_group`](#vrrp_sync_group)
* [`lvs_real_server`](#lvs_real_server)
* [`lvs_virtual_server`](#lvs_virtual_server)

##### <a name="sysconf_dir"></a>`sysconf_dir`

Data type: `String[1]`



##### <a name="sysconf_options"></a>`sysconf_options`

Data type: `String`



##### <a name="config_dir"></a>`config_dir`

Data type: `Stdlib::Absolutepath`



Default value: `'/etc/keepalived'`

##### <a name="config_dir_mode"></a>`config_dir_mode`

Data type: `Stdlib::Filemode`



Default value: `'0755'`

##### <a name="config_file_mode"></a>`config_file_mode`

Data type: `Stdlib::Filemode`



Default value: `'0644'`

##### <a name="config_group"></a>`config_group`

Data type: `String[1]`



Default value: `'root'`

##### <a name="config_owner"></a>`config_owner`

Data type: `String[1]`



Default value: `'root'`

##### <a name="daemon_group"></a>`daemon_group`

Data type: `String[1]`



Default value: `'root'`

##### <a name="daemon_user"></a>`daemon_user`

Data type: `String[1]`



Default value: `'root'`

##### <a name="pkg_ensure"></a>`pkg_ensure`

Data type: `String[1]`



Default value: `'present'`

##### <a name="pkg_list"></a>`pkg_list`

Data type: `Array[String[1]]`



Default value: `['keepalived']`

##### <a name="service_enable"></a>`service_enable`

Data type: `Boolean`



Default value: ``true``

##### <a name="service_ensure"></a>`service_ensure`

Data type: `Stdlib::Ensure::Service`



Default value: `'running'`

##### <a name="service_hasrestart"></a>`service_hasrestart`

Data type: `Boolean`



##### <a name="service_hasstatus"></a>`service_hasstatus`

Data type: `Boolean`



##### <a name="service_manage"></a>`service_manage`

Data type: `Boolean`



Default value: ``true``

##### <a name="service_name"></a>`service_name`

Data type: `String[1]`



Default value: `'keepalived'`

##### <a name="service_restart"></a>`service_restart`

Data type: `Optional[String[1]]`



Default value: ``undef``

##### <a name="vrrp_instance"></a>`vrrp_instance`

Data type: `Hash`



Default value: `{}`

##### <a name="vrrp_script"></a>`vrrp_script`

Data type: `Hash`



Default value: `{}`

##### <a name="vrrp_track_process"></a>`vrrp_track_process`

Data type: `Hash`



Default value: `{}`

##### <a name="vrrp_sync_group"></a>`vrrp_sync_group`

Data type: `Hash`



Default value: `{}`

##### <a name="lvs_real_server"></a>`lvs_real_server`

Data type: `Hash`



Default value: `{}`

##### <a name="lvs_virtual_server"></a>`lvs_virtual_server`

Data type: `Hash`



Default value: `{}`

### <a name="keepalivedconfig"></a>`keepalived::config`

Configure keepalived module

### <a name="keepalivedglobal_defs"></a>`keepalived::global_defs`

Manage keepalived notifictions

#### Parameters

The following parameters are available in the `keepalived::global_defs` class:

* [`notification_email`](#notification_email)
* [`notification_email_from`](#notification_email_from)
* [`smtp_server`](#smtp_server)
* [`smtp_connect_timeout`](#smtp_connect_timeout)
* [`router_id`](#router_id)
* [`script_user`](#script_user)
* [`enable_script_security`](#enable_script_security)
* [`snmp_socket`](#snmp_socket)
* [`enable_snmp_keepalived`](#enable_snmp_keepalived)
* [`enable_snmp_vrrp`](#enable_snmp_vrrp)
* [`enable_snmp_checker`](#enable_snmp_checker)
* [`enable_snmp_rfc`](#enable_snmp_rfc)
* [`enable_snmp_rfcv2`](#enable_snmp_rfcv2)
* [`enable_snmp_rfcv3`](#enable_snmp_rfcv3)
* [`enable_traps`](#enable_traps)
* [`enable_dbus`](#enable_dbus)
* [`vrrp_higher_prio_send_advert`](#vrrp_higher_prio_send_advert)
* [`vrrp_garp_lower_prio_repeat`](#vrrp_garp_lower_prio_repeat)
* [`vrrp_garp_master_refresh`](#vrrp_garp_master_refresh)
* [`vrrp_garp_lower_prio_delay`](#vrrp_garp_lower_prio_delay)
* [`vrrp_startup_delay`](#vrrp_startup_delay)

##### <a name="notification_email"></a>`notification_email`

Data type: `Any`

Array of notification email Recipients.

Default value: ``undef``

##### <a name="notification_email_from"></a>`notification_email_from`

Data type: `Any`

Define the notification email Sender.

Default value: ``undef``

##### <a name="smtp_server"></a>`smtp_server`

Data type: `Any`

Define the smtp server addres.

Default value: ``undef``

##### <a name="smtp_connect_timeout"></a>`smtp_connect_timeout`

Data type: `Any`

Define the smtp connect timeout.

Default value: ``undef``

##### <a name="router_id"></a>`router_id`

Data type: `Any`

Define the router ID.

Default value: ``undef``

##### <a name="script_user"></a>`script_user`

Data type: `Any`

Set the global script_user option.

Default value: ``undef``

##### <a name="enable_script_security"></a>`enable_script_security`

Data type: `Any`

Set the enable_script_security option.

Default value: ``undef``

##### <a name="snmp_socket"></a>`snmp_socket`

Data type: `Any`

Define snmp master agent socker

Default value: `'unix:/var/agentx/master'`

##### <a name="enable_snmp_keepalived"></a>`enable_snmp_keepalived`

Data type: `Any`

Set enable_snmp_keepalived option.

Default value: ``undef``

##### <a name="enable_snmp_vrrp"></a>`enable_snmp_vrrp`

Data type: `Any`

Set enable_snmp_vrrp option.

Default value: ``undef``

##### <a name="enable_snmp_checker"></a>`enable_snmp_checker`

Data type: `Any`

Set enable_snmp_checker option

Default value: ``undef``

##### <a name="enable_snmp_rfc"></a>`enable_snmp_rfc`

Data type: `Any`

Set enable_snmp_rfc option.

Default value: ``undef``

##### <a name="enable_snmp_rfcv2"></a>`enable_snmp_rfcv2`

Data type: `Any`

Set enable_snmp_rfcv2 option.

Default value: ``undef``

##### <a name="enable_snmp_rfcv3"></a>`enable_snmp_rfcv3`

Data type: `Any`

Set enable_snmp_rfcv3 option.

Default value: ``undef``

##### <a name="enable_traps"></a>`enable_traps`

Data type: `Any`

Set enable_traps option.

Default value: ``undef``

##### <a name="enable_dbus"></a>`enable_dbus`

Data type: `Boolean`

Set enable_dbus option

Default value: ``false``

##### <a name="vrrp_higher_prio_send_advert"></a>`vrrp_higher_prio_send_advert`

Data type: `Optional[Boolean]`

Set vrrp_higher_prio_send_advert option.

Default value: ``undef``

##### <a name="vrrp_garp_lower_prio_repeat"></a>`vrrp_garp_lower_prio_repeat`

Data type: `Optional[Integer]`

Set vrrp_garp_lower_prio_repeat option.

Default value: ``undef``

##### <a name="vrrp_garp_master_refresh"></a>`vrrp_garp_master_refresh`

Data type: `Optional[Integer]`

Set vrrp_garp_master_refresh option.

Default value: ``undef``

##### <a name="vrrp_garp_lower_prio_delay"></a>`vrrp_garp_lower_prio_delay`

Data type: `Optional[Integer]`

Set vrrp_garp_lower_prio_delay option.

Default value: ``undef``

##### <a name="vrrp_startup_delay"></a>`vrrp_startup_delay`

Data type: `Optional[Float]`

Set vrrp_startup_delay option.

Default value: ``undef``

### <a name="keepalivedinstall"></a>`keepalived::install`

Install keepalived package

### <a name="keepalivedservice"></a>`keepalived::service`

Manage keepalived service

## Defined types

### <a name="keepalivedlvsreal_server"></a>`keepalived::lvs::real_server`

Add a real server to a Linux Virtual Server with keepalived

#### Parameters

The following parameters are available in the `keepalived::lvs::real_server` defined type:

* [`virtual_server`](#virtual_server)
* [`ip_address`](#ip_address)
* [`port`](#port)
* [`options`](#options)

##### <a name="virtual_server"></a>`virtual_server`

Data type: `String[1]`

The name of the virtual server this real server will be added to

##### <a name="ip_address"></a>`ip_address`

Data type: `Stdlib::IP::Address`

The ip address of the real server

##### <a name="port"></a>`port`

Data type: `Stdlib::Port`

Real sever IP port.  (if ommitted the port defaults to the VIP port)

##### <a name="options"></a>`options`

Data type: `Keepalived::Options`

One or more options to include in the real_server block

@example
  options => {
    inhibit_on_failure => true,
    SMTP_CHECK => {
      connect_timeout => 10
      host => {
        connect_ip => '127.0.0.1'
      }
    }
  }

Default value: `{}`

### <a name="keepalivedlvsvirtual_server"></a>`keepalived::lvs::virtual_server`

Configure a Linux Virtual Server with keepalived

Work in progress, supports:
  - single IP/port virtual servers
  - TCP_CHECK healthchecks

#### Examples

##### 

```puppet
real_server_options => {
  inhibit_on_failure => true,
  SMTP_CHECK => {
    connect_timeout => 10
    host => {
      connect_ip => '127.0.0.1'
    }
  }
}
```

#### Parameters

The following parameters are available in the `keepalived::lvs::virtual_server` defined type:

* [`ip_address`](#ip_address)
* [`port`](#port)
* [`fwmark`](#fwmark)
* [`lb_algo`](#lb_algo)
* [`delay_loop`](#delay_loop)
* [`protocol`](#protocol)
* [`lb_kind`](#lb_kind)
* [`ha_suspend`](#ha_suspend)
* [`alpha`](#alpha)
* [`omega`](#omega)
* [`sh_port`](#sh_port)
* [`sh_fallback`](#sh_fallback)
* [`quorum`](#quorum)
* [`quorum_up`](#quorum_up)
* [`quorum_down`](#quorum_down)
* [`hysteresis`](#hysteresis)
* [`tcp_check`](#tcp_check)
* [`real_server_options`](#real_server_options)
* [`sorry_server`](#sorry_server)
* [`sorry_server_inhibit`](#sorry_server_inhibit)
* [`persistence_timeout`](#persistence_timeout)
* [`virtualhost`](#virtualhost)
* [`real_servers`](#real_servers)
* [`collect_exported`](#collect_exported)

##### <a name="ip_address"></a>`ip_address`

Data type: `Optional[Stdlib::IP::Address]`

Virtual server IP address.

Default value: ``undef``

##### <a name="port"></a>`port`

Data type: `Optional[Stdlib::Port]`

Virtual sever IP port.

Default value: ``undef``

##### <a name="fwmark"></a>`fwmark`

Data type: `Optional[Integer[1]]`

Virtual Server firewall mark. (overrides ip_address and port)

Default value: ``undef``

##### <a name="lb_algo"></a>`lb_algo`

Data type: `Enum['rr','wrr','lc','wlc','lblc','sh','dh']`

Must be one of rr, wrr, lc, wlc, lblc, sh, dh

##### <a name="delay_loop"></a>`delay_loop`

Data type: `Optional[Integer[1]]`



Default value: ``undef``

##### <a name="protocol"></a>`protocol`

Data type: `Enum['TCP','UDP']`



Default value: `'TCP'`

##### <a name="lb_kind"></a>`lb_kind`

Data type: `Enum['NAT','DR','TUN']`

Must be one of NAT, TUN, DR.

Default value: `'NAT'`

##### <a name="ha_suspend"></a>`ha_suspend`

Data type: `Boolean`



Default value: ``false``

##### <a name="alpha"></a>`alpha`

Data type: `Boolean`



Default value: ``false``

##### <a name="omega"></a>`omega`

Data type: `Boolean`



Default value: ``false``

##### <a name="sh_port"></a>`sh_port`

Data type: `Boolean`



Default value: ``false``

##### <a name="sh_fallback"></a>`sh_fallback`

Data type: `Boolean`



Default value: ``false``

##### <a name="quorum"></a>`quorum`

Data type: `Optional[Integer[1]]`



Default value: ``undef``

##### <a name="quorum_up"></a>`quorum_up`

Data type: `Optional[String[1]]`



Default value: ``undef``

##### <a name="quorum_down"></a>`quorum_down`

Data type: `Optional[String[1]]`



Default value: ``undef``

##### <a name="hysteresis"></a>`hysteresis`

Data type: `Optional[Integer[0]]`



Default value: ``undef``

##### <a name="tcp_check"></a>`tcp_check`

Data type: `Optional[Hash]`

The TCP_CHECK to configure for real_servers.

Default value: ``undef``

##### <a name="real_server_options"></a>`real_server_options`

Data type: `Hash`

One or more options to apply to all real_server blocks inside this virtual_server.

Default value: `{}`

##### <a name="sorry_server"></a>`sorry_server`

Data type: `Optional[Struct[{ ip_address => Stdlib::IP::Address, port => Stdlib::Port }]]`

The sorry_server to define

Default value: ``undef``

##### <a name="sorry_server_inhibit"></a>`sorry_server_inhibit`

Data type: `Boolean`



Default value: ``false``

##### <a name="persistence_timeout"></a>`persistence_timeout`

Data type: `Optional[Integer[1]]`



Default value: ``undef``

##### <a name="virtualhost"></a>`virtualhost`

Data type: `Optional[Stdlib::Fqdn]`



Default value: ``undef``

##### <a name="real_servers"></a>`real_servers`

Data type: `Array[Hash]`

The real servers to balance to.

Default value: `[]`

##### <a name="collect_exported"></a>`collect_exported`

Data type: `Boolean`

Boolean. Automatically collect exported @@keepalived::lvs::real_servers
with a virtual_server equal to the name/title of this resource. This allows
you to easily export a real_server resource on each node in the pool.

Default value: ``true``

### <a name="keepalivedvrrpinstance"></a>`keepalived::vrrp::instance`

Configure VRRP instance

#### Examples

##### 

```puppet
May be specified as either:
a) ip address (or array of IP addresses)
   e.g. `'10.0.0.1'`
b) a hash (or array of hashes) containing
   extra properties
   e.g. `{ 'ip' => '10.0.0.1', 'label' => 'webvip' }`
   Supported properties: dev, brd, label, scope.
```

##### 

```puppet
May be specified as a hash (or array of hashes)
  containing extra properties
    e.g. `{ 'src' => '10.0.0.1',
            'to' => '192.168.30.0/24',
            'via' => '10.0.0.254',
            'metric' => '15' }`
Supported properties: src, to, via, dev, scope, table, metric
```

##### 

```puppet
May be specified as a hash (or array of hashes)
   containing extra properties
   e.g. `{ 'from' => '10.0.0.1',
           'via' => '10.0.0.254',
           'lookup' => 'customroute',
           'metric' => '15' }`
   Supported properties: from, to, dev, lookup, metric
```

##### 

```puppet
May be specified as either:
a) ip address (or array of IP addresses)
   e.g. `'10.0.0.1'`
b) a hash (or array of hashes) containing
   extra properties
e.g. `{ 'ip'=>'10.0.0.1', 'scope'=>'local' }`
Supported properties: dev, brd, label, scope.
```

#### Parameters

The following parameters are available in the `keepalived::vrrp::instance` defined type:

* [`interface`](#interface)
* [`priority`](#priority)
* [`state`](#state)
* [`virtual_ipaddress_int`](#virtual_ipaddress_int)
* [`virtual_ipaddress`](#virtual_ipaddress)
* [`virtual_routes`](#virtual_routes)
* [`virtual_rules`](#virtual_rules)
* [`virtual_ipaddress_excluded`](#virtual_ipaddress_excluded)
* [`virtual_router_id`](#virtual_router_id)
* [`auth_type`](#auth_type)
* [`auth_pass`](#auth_pass)
* [`track_script`](#track_script)
* [`track_process`](#track_process)
* [`track_interface`](#track_interface)
* [`lvs_interface`](#lvs_interface)
* [`smtp_alert`](#smtp_alert)
* [`nopreempt`](#nopreempt)
* [`preempt_delay`](#preempt_delay)
* [`advert_int`](#advert_int)
* [`garp_master_delay`](#garp_master_delay)
* [`garp_master_refresh`](#garp_master_refresh)
* [`notify_script_master`](#notify_script_master)
* [`notify_script_backup`](#notify_script_backup)
* [`notify_script_fault`](#notify_script_fault)
* [`notify_script_stop`](#notify_script_stop)
* [`notify_script`](#notify_script)
* [`multicast_source_ip`](#multicast_source_ip)
* [`notify_script_master_rx_lower_pri`](#notify_script_master_rx_lower_pri)
* [`unicast_source_ip`](#unicast_source_ip)
* [`unicast_peers`](#unicast_peers)
* [`dont_track_primary`](#dont_track_primary)
* [`use_vmac`](#use_vmac)
* [`vmac_xmit_base`](#vmac_xmit_base)
* [`native_ipv6`](#native_ipv6)
* [`garp_lower_prio_repeat`](#garp_lower_prio_repeat)
* [`higher_prio_send_advert`](#higher_prio_send_advert)
* [`collect_unicast_peers`](#collect_unicast_peers)

##### <a name="interface"></a>`interface`

Data type: `Any`

Define which interface to listen on.

##### <a name="priority"></a>`priority`

Data type: `Integer[1,254]`

Set instance priority.

##### <a name="state"></a>`state`

Data type: `Any`

Set instance state.

##### <a name="virtual_ipaddress_int"></a>`virtual_ipaddress_int`

Data type: `Any`

Set interface for VIP to be assigned to,

Default value: ``undef``

##### <a name="virtual_ipaddress"></a>`virtual_ipaddress`

Data type: `Any`

Set floating IP address.

Default value: ``undef``

##### <a name="virtual_routes"></a>`virtual_routes`

Data type: `Any`

Set floating routes.

Default value: ``undef``

##### <a name="virtual_rules"></a>`virtual_rules`

Data type: `Optional[Array[Keepalived::Vrrp::Instance::VRule]]`

Set floating rules.

Default value: ``undef``

##### <a name="virtual_ipaddress_excluded"></a>`virtual_ipaddress_excluded`

Data type: `Any`

For cases with large numbers (eg 200) of IPs
on the same interface. To decrease the number
of packets sent in adverts, you can exclude
most IPs from adverts.

Default value: ``undef``

##### <a name="virtual_router_id"></a>`virtual_router_id`

Data type: `Integer[1,255]`

Set virtual router id.

##### <a name="auth_type"></a>`auth_type`

Data type: `Any`

Set authentication method.

Default value: ``undef``

##### <a name="auth_pass"></a>`auth_pass`

Data type: `Optional[Variant[String, Sensitive[String]]]`

Authentication password.

Default value: ``undef``

##### <a name="track_script"></a>`track_script`

Data type: `Any`

Define which script to run to track service states.

Default value: ``undef``

##### <a name="track_process"></a>`track_process`

Data type: `Optional[Array[String[1]]]`

Define which process trackers to run.

Default value: ``undef``

##### <a name="track_interface"></a>`track_interface`

Data type: `Any`

Define which interface(s) to monitor.
Go to FAULT state if one of
these interfaces goes down.
May be specified as either:
  a) interface name
  b) array of interfaces names

Default value: ``undef``

##### <a name="lvs_interface"></a>`lvs_interface`

Data type: `Any`

Define lvs_sync_daemon_interface.

Default value: ``undef``

##### <a name="smtp_alert"></a>`smtp_alert`

Data type: `Any`

Send status alerts via SMTP. Requires user provided
in SMTP settings in keepalived::global_defs class.

Default value: ``false``

##### <a name="nopreempt"></a>`nopreempt`

Data type: `Any`

Allows the lower priority machine to maintain
the master role, when a higher priority machine
comes back online.
NOTE: For this to work, the initial state of this
entry must be BACKUP

Default value: ``false``

##### <a name="preempt_delay"></a>`preempt_delay`

Data type: `Any`

Seconds after startup until preemption
Range: 0 to 1,000
NOTE: For this to work, the initial state of this
entry must be BACKUP

Default value: ``undef``

##### <a name="advert_int"></a>`advert_int`

Data type: `Any`

The interval between VRRP packets

Default value: `1`

##### <a name="garp_master_delay"></a>`garp_master_delay`

Data type: `Any`

The delay for gratuitous ARP after transition
to MASTER

Default value: `5`

##### <a name="garp_master_refresh"></a>`garp_master_refresh`

Data type: `Any`

Repeat gratuitous ARP after transition to MASTER
this often.

Default value: ``undef``

##### <a name="notify_script_master"></a>`notify_script_master`

Data type: `Any`

Define the notify master script.

Default value: ``undef``

##### <a name="notify_script_backup"></a>`notify_script_backup`

Data type: `Any`

Define the notify backup script.

Default value: ``undef``

##### <a name="notify_script_fault"></a>`notify_script_fault`

Data type: `Any`

Define the notify fault script.

Default value: ``undef``

##### <a name="notify_script_stop"></a>`notify_script_stop`

Data type: `Any`

Define the notify stop script.

Default value: ``undef``

##### <a name="notify_script"></a>`notify_script`

Data type: `Any`

Define the notify script.

Default value: ``undef``

##### <a name="multicast_source_ip"></a>`multicast_source_ip`

Data type: `Any`

default IP for binding vrrpd is the primary IP
on interface. If you want to hide the location of vrrpd,
use this IP as src_addr for multicast vrrp packets.

Default value: ``undef``

##### <a name="notify_script_master_rx_lower_pri"></a>`notify_script_master_rx_lower_pri`

Data type: `Optional[Stdlib::Absolutepath]`

Define the notify_master_rx_lower_pri script.
This is executed if a master receives an advert with
priority lower than the master's advert.

Default value: ``undef``

##### <a name="unicast_source_ip"></a>`unicast_source_ip`

Data type: `Optional[Stdlib::IP::Address]`

default IP for binding vrrpd is the primary IP
on interface. If you want to hide the location of vrrpd,
use this IP as src_addr for unicast vrrp packets.

Default value: ``undef``

##### <a name="unicast_peers"></a>`unicast_peers`

Data type: `Variant[Array[Stdlib::IP::Address], Stdlib::IP::Address]`

Do not send VRRP adverts over VRRP multicast group.
Instead send adverts to the list of ip addresses using
a unicast design fashion.

May be specified as an array with ip addresses

Default value: `[]`

##### <a name="dont_track_primary"></a>`dont_track_primary`

Data type: `Any`

Tells keepalived to ignore VRRP interface faults.
Can be useful on setup where two routers are
connected directly to each other on the interface
used for VRRP. Without this feature the link down
caused by one router crashing would also inspire
the other router to lose (or not gain) MASTER state,
since it was also tracking link status.
Default: false.

Default value: ``false``

##### <a name="use_vmac"></a>`use_vmac`

Data type: `Any`

Use virtual MAC address for virtual IP addresses.

Default value: ``false``

##### <a name="vmac_xmit_base"></a>`vmac_xmit_base`

Data type: `Any`

When using virtual MAC addresses transmit and receive
VRRP messaged on the underlying interface whilst ARP
will happen from the the VMAC interface.

Default value: ``true``

##### <a name="native_ipv6"></a>`native_ipv6`

Data type: `Boolean`

Force instance to use IPv6 (when mixed IPv4 and IPv6 config)

Default value: ``false``

##### <a name="garp_lower_prio_repeat"></a>`garp_lower_prio_repeat`

Data type: `Optional[Integer]`



Default value: ``undef``

##### <a name="higher_prio_send_advert"></a>`higher_prio_send_advert`

Data type: `Optional[Boolean]`



Default value: ``undef``

##### <a name="collect_unicast_peers"></a>`collect_unicast_peers`

Data type: `Boolean`



Default value: ``false``

### <a name="keepalivedvrrpscript"></a>`keepalived::vrrp::script`

Configure VRRP script

#### Parameters

The following parameters are available in the `keepalived::vrrp::script` defined type:

* [`interval`](#interval)
* [`script`](#script)
* [`weight`](#weight)
* [`fall`](#fall)
* [`rise`](#rise)
* [`timeout`](#timeout)
* [`user`](#user)
* [`group`](#group)
* [`no_weight`](#no_weight)

##### <a name="interval"></a>`interval`

Data type: `Any`

Set the interval to run the vrrp script.

Default value: `'2'`

##### <a name="script"></a>`script`

Data type: `String[1]`

Which command or script to execute.

##### <a name="weight"></a>`weight`

Data type: `Any`

The weight the script should add to the instance.

Default value: ``undef``

##### <a name="fall"></a>`fall`

Data type: `Any`

required number of failures for KO switch.

Default value: ``undef``

##### <a name="rise"></a>`rise`

Data type: `Any`

required number of successes for OK switch.

Default value: ``undef``

##### <a name="timeout"></a>`timeout`

Data type: `Any`

max time to wait for the vrrp script to return.

Default value: ``undef``

##### <a name="user"></a>`user`

Data type: `Any`

user to run the vrrp script under.

Default value: ``undef``

##### <a name="group"></a>`group`

Data type: `Any`

group to run the vrrp script under - only used if $user is also set.

Default value: ``undef``

##### <a name="no_weight"></a>`no_weight`

Data type: `Any`



Default value: ``false``

### <a name="keepalivedvrrpsync_group"></a>`keepalived::vrrp::sync_group`

Configure the group for instance

#### Parameters

The following parameters are available in the `keepalived::vrrp::sync_group` defined type:

* [`group`](#group)
* [`notify_script_master`](#notify_script_master)
* [`notify_script_backup`](#notify_script_backup)
* [`notify_script_fault`](#notify_script_fault)
* [`notify_script`](#notify_script)
* [`notify_script_master_rx_lower_pri`](#notify_script_master_rx_lower_pri)
* [`smtp_alert`](#smtp_alert)
* [`nopreempt`](#nopreempt)
* [`global_tracking`](#global_tracking)

##### <a name="group"></a>`group`

Data type: `Any`

Define vrrp instances to group (Array)

##### <a name="notify_script_master"></a>`notify_script_master`

Data type: `Any`

Define the notify master script.

Default value: ``undef``

##### <a name="notify_script_backup"></a>`notify_script_backup`

Data type: `Any`

Define the notify backup script.

Default value: ``undef``

##### <a name="notify_script_fault"></a>`notify_script_fault`

Data type: `Any`

Define the notify fault script.

Default value: ``undef``

##### <a name="notify_script"></a>`notify_script`

Data type: `Any`

Define the notify script.

Default value: ``undef``

##### <a name="notify_script_master_rx_lower_pri"></a>`notify_script_master_rx_lower_pri`

Data type: `Optional[Stdlib::Absolutepath]`

Define the notify_master_rx_lower_pri script.
This is executed if a master receives an advert with
priority lower than the master's advert.

Default value: ``undef``

##### <a name="smtp_alert"></a>`smtp_alert`

Data type: `Any`

Send email on status change

Default value: ``undef``

##### <a name="nopreempt"></a>`nopreempt`

Data type: `Any`



Default value: ``undef``

##### <a name="global_tracking"></a>`global_tracking`

Data type: `Boolean`



Default value: ``false``

### <a name="keepalivedvrrptrack_process"></a>`keepalived::vrrp::track_process`

Configure the process tracker

#### Parameters

The following parameters are available in the `keepalived::vrrp::track_process` defined type:

* [`proc_name`](#proc_name)
* [`weight`](#weight)
* [`quorum`](#quorum)
* [`delay`](#delay)
* [`full_command`](#full_command)
* [`param_match`](#param_match)

##### <a name="proc_name"></a>`proc_name`

Data type: `String[1]`

process name to track

##### <a name="weight"></a>`weight`

Data type: `Optional[Integer[0]]`

The weight that should add to the instance.

Default value: ``undef``

##### <a name="quorum"></a>`quorum`

Data type: `Integer[0]`

Number of processes to expect running

Default value: `1`

##### <a name="delay"></a>`delay`

Data type: `Optional[Integer[0]]`

Time to delay after process quorum lost before considering process failed (in fractions of second)

Default value: ``undef``

##### <a name="full_command"></a>`full_command`

Data type: `Boolean`

Match entire process cmdline

Default value: ``false``

##### <a name="param_match"></a>`param_match`

Data type: `Optional[Enum['initial','partial']]`

Set inital if command has no parameters or use partial if first n parameters match

Default value: ``undef``

## Data types

### <a name="keepalivedoptions"></a>`Keepalived::Options`

keepalived::options

Alias of

```puppet
Hash[String[1], Any]
```

### <a name="keepalivedvrrpinstancevrule"></a>`Keepalived::Vrrp::Instance::VRule`

keepalived::vrrp::instance::vrule

Alias of

```puppet
Struct[{
    Optional[from]   => String,
    Optional[to]     => String,
    Optional[dev]    => String,
    Optional[lookup] => String
}]
```


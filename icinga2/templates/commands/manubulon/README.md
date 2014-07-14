Monitoring
==========

Icinga2 check commands for <a href="http://nagios.manubulon.com/index_snmp.html"> snmp manubulon </a> plugins.

### Checks you can make by host type

**N/A**      : nothing of this type to check.

**SNMP**     : yes with simple snmp query.

**??**       : not tested because useless most of the time.

**Specific** : name of the script to look at for platform specific checks.


  Host type               | Interface  | storage  | load/cpu  | mem | process  | env | specific
  ------------------------|------------|----------|-----------|-----|----------|-----|-------------------------
  Linux                   |   Yes      |   Yes    |   Yes     | Yes |   Yes    | No  |
  Windows                 |   Yes      |   Yes    |   Yes     | Yes |   Yes    | No  | check_snmp_win.pl
  Cisco router/switch     |   Yes      |   N/A    |   Yes     | Yes |   N/A    | Yes |
  HP router/switch        |   Yes      |   N/A    |   Yes     | Yes |   N/A    | No  |
  Bluecoat proxy          |   Yes      |   snmp   |   Yes     | snmp|   No     | Yes |
  CheckPoint on SPLAT     |   Yes      |   Yes    |   Yes     | Yes |   Yes    | No  | check_snmp_cpfw.pl
  CheckPoint on Nokia IP  |   Yes      |   Yes    |   Yes     | No  |   ??     | No  | check_snmp_vrrp.pl
  Boostedge               |   Yes      |   Yes    |   Yes     | Yes |   ??     | No  | check_snmp_boostedge.pl
  AS400                   |   Yes      |   Yes    |   Yes     | Yes |   No     | No  |
  NetsecureOne Netbox     |   Yes      |   Yes    |   Yes     | ??  |   Yes    | No  |
  Radware Linkproof       |   Yes      |   N/A    |   snmp    | snmp|   No     | No  | check_snmp_linkproof_nhr <br> check_snmp_vrrp.pl
  IronPort                |   Yes      |   snmp   |   snmp    | snmp|   No     | Yes |
  Cisco CSS               |   Yes      |   ??     |   Yes     | Yes |   No     | ??  | check_snmp_css.pl

## <a id="plugin-check-commands"></a> Plugin Check Commands

#### <a id="plugin-check-command-snmp-load"></a> snmp load

Check command object for the `check_snmp_load.pl` plugin.

Custom Attributes:

Name                | Description
--------------------|--------------
snmp_address        | **Optional.** The host's address. Defaults to "$address$".
snmp_community      | **Optional.** The SNMP community. Defaults to "public".
snmp_port           | **Optional.** The SNMP port connection.
snmp_v2c            | **Optional.** SNMP version to 2c. Defaults to "false".
snmp_warn           | **Optional.** The warning threshold.
snmp_crit           | **Optional.** The critical threshold.
snmp_load_type      | **Optional.** Load type. Default  to "stand". Check all availables <a href="http://nagios.manubulon.com/snmp_load.html">snmp load</a>
snmp_perf           | **Optional.** Enable perfdata values. Defaults to "true"

#### <a id="plugin-check-command-snmp-memory"></a> snmp memory

Check command object for the `check_snmp_mem.pl` plugin.

Custom Attributes:

Name                | Description
--------------------|--------------
snmp_address        | **Optional.** The host's address. Defaults to "$address$".
snmp_community      | **Optional.** The SNMP community. Defaults to "public".
snmp_port           | **Optional.** The SNMP port connection.
snmp_v2c            | **Optional.** SNMP version to 2c. Defaults to "false".
snmp_warn           | **Optional.** The warning threshold.
snmp_crit           | **Optional.** The critical threshold.
snmp_perf           | **Optional.** Enable perfdata values. Defaults to "true"

#### <a id="plugin-check-command-snmp-storage"></a> snmp storage

Check command object for the `check_snmp_storage.pl` plugin.

Custom Attributes:

Name                | Description
--------------------|--------------
snmp_address        | **Optional.** The host's address. Defaults to "$address$".
snmp_community      | **Optional.** The SNMP community. Defaults to "public".
snmp_port           | **Optional.** The SNMP port connection.
snmp_v2c            | **Optional.** SNMP version to 2c. Defaults to "false".
snmp_warn           | **Optional.** The warning threshold.
snmp_crit           | **Optional.** The critical threshold.
snmp_storage_name   | **Optional.** Storage name. Default to regex "^/$$". Check more options in <a href="http://nagios.manubulon.com/snmp_storage.html">snmp storage</a>
snmp_perf           | **Optional.** Enable perfdata values. Defaults to "true"

#### <a id="plugin-check-command-snmp-int"></a> snmp int

Check command object for the `check_snmp_int.pl` plugin.

Custom Attributes:

Name                  | Description
----------------------|--------------
snmp_address          | **Optional.** The host's address. Defaults to "$address$".
snmp_community        | **Optional.** The SNMP community. Defaults to "public".
snmp_port             | **Optional.** The SNMP port connection.
snmp_v2c              | **Optional.** SNMP version to 2c. Defaults to "false".
snmp_warn             | **Optional.** The warning threshold.
snmp_crit             | **Optional.** The critical threshold.
snmp_interface        | **Optional.** Network interface name. Default to regex "eth0".
snmp_interface_perf   | **Optional.** Check the input/ouput bandwidth of the interface. Defaults to "true"
snmp_interface_bits   | **Optional.** Make the warning and critical levels in KBits/s. Defaults to "true"
snmp_interface_64bit  | **Optional.** Use 64 bits counters instead of the standard counters when checking bandwidth & performance data for interface >= 1Gbps. Defaults to "false"
snmp_perf             | **Optional.** Enable perfdata values. Defaults to "true"

#### <a id="plugin-check-command-snmp-process"></a> snmp process

Check command object for the `check_snmp_process.pl` plugin.

Custom Attributes:

Name                  | Description
----------------------|--------------
snmp_address          | **Optional.** The host's address. Defaults to "$address$".
snmp_community        | **Optional.** The SNMP community. Defaults to "public".
snmp_port             | **Optional.** The SNMP port connection.
snmp_v2c              | **Optional.** SNMP version to 2c. Defaults to "false".
snmp_warn             | **Optional.** The warning threshold.
snmp_crit             | **Optional.** The critical threshold.
snmp_process_name     | **Optional.** Name of the process (regexp). No trailing slash!. Defaults to ".*"
snmp_perf             | **Optional.** Enable perfdata values. Defaults to "true"

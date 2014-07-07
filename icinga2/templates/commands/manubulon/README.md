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

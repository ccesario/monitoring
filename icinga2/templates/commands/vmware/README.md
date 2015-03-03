Monitoring
==========

## <a id="plugin-check-commands"></a> VMware
Icinga2 check commands for [vmware esx](https://github.com/BaldMansMojo/check_vmware_esx) plugins.

#### <a id="plugin-check-command-vmware-esx-dc-volumes"></a> vmware-esx-dc-volumes

Check command object for the `check_vmware_esx` plugin. Shows all datastore volumes info.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_subselect        | **Optional.** Volume name to be checked the free space.
vmware_gigabyte         | **Optional.** Output in GB instead of MB.
vmware_usedspace        | **Optional.** Output used space instead of free. Defaults to "false".
vmware_alertonly        | **Optional.** List only alerting volumes. Defaults to "false".
vmware_exclude          | **Optional.** Blacklist volumes name. No value defined as default.
vmware_include          | **Optional.** Whitelist volumes name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_dc_volume_used   | **Optional.** Output used space instead of free. Defaults to "true".
vmware_warn             | **Optional.** The warning threshold for volumes. Defaults to "80%".
vmware_crit             | **Optional.** The critical threshold for volumes. Defaults to "90%".


#### <a id="plugin-check-command-vmware-esx-dc-runtime-info"></a> vmware-esx-dc-runtime-info

Check command object for the `check_vmware_esx` plugin. Shows all runtime info for the datacenter/Vcenter.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-dc-runtime-listvms"></a> vmware-esx-dc-runtime-listvms

Check command object for the `check_vmware_esx` plugin. List of vmware machines and their power state. BEWARE!! In larger environments systems can cause trouble displaying the informations needed due to the mass of data. Use **vmware_alertonly** to avoid this.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_alertonly        | **Optional.** List only alerting VMs. Important here to avoid masses of data.
vmware_exclude          | **Optional.** Blacklist VMs name. No value defined as default.
vmware_include          | **Optional.** Whitelist VMs name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-dc-runtime-listhost"></a> vmware-esx-dc-runtime-listhost

Check command object for the `check_vmware_esx` plugin. List of VMware ESX hosts and their power state.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_alertonly        | **Optional.** List only alerting hosts. Important here to avoid masses of data.
vmware_exclude          | **Optional.** Blacklist VMware ESX hosts. No value defined as default.
vmware_include          | **Optional.** Whitelist VMware ESX hosts. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-dc-runtime-listcluster"></a> vmware-esx-dc-runtime-listcluster

Check command object for the `check_vmware_esx` plugin. List of VMware clusters and their states.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_alertonly        | **Optional.** List only alerting hosts. Important here to avoid masses of data.
vmware_exclude          | **Optional.** Blacklist VMware cluster. No value defined as default.
vmware_include          | **Optional.** Whitelist VMware cluster. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-dc-runtime-issues"></a> vmware-esx-dc-runtime-issues

Check command object for the `check_vmware_esx` plugin. All issues for the host.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist issues. No value defined as default.
vmware_include          | **Optional.** Whitelist issues. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-dc-runtime-status"></a> vmware-esx-dc-runtime-status

Check command object for the `check_vmware_esx` plugin. Overall object status (gray/green/red/yellow).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-dc-runtime-tools"></a> vmware-esx-dc-runtime-tools

Check command object for the `check_vmware_esx` plugin. Vmware Tools status.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_datacenter       | **Required.** Datacenter/vCenter hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_poweredonly      | **Optional.** List only VMs which are powered on. No value defined as default.
vmware_alertonly        | **Optional.** List only alerting VMs. Important here to avoid masses of data.
vmware_exclude          | **Optional.** Blacklist VMs. No value defined as default.
vmware_include          | **Optional.** Whitelist VMs. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-check"></a> vmware-esx-soap-host-check

Check command object for the `check_vmware_esx` plugin. Simple check to verify a successfull connection to VMware SOAP API.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-uptime"></a> vmware-esx-soap-host-uptime

Check command object for the `check_vmware_esx` plugin. Displays uptime of the VMware host.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-cpu"></a> vmware-esx-soap-host-cpu

Check command object for the `check_vmware_esx` plugin. CPU usage in percentage.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. Defaults to "80%".
vmware_crit             | **Optional.** The critical threshold in percent. Defaults to "90%".


#### <a id="plugin-check-command-vmware-esx-soap-host-cpu-ready"></a> vmware-esx-soap-host-cpu-ready

Check command object for the `check_vmware_esx` plugin. Percentage of time that the virtual machine was ready, but could not get scheduled to run on the physical CPU. CPU ready time is dependent on the number of virtual machines on the host and their CPU loads. High or growing ready time can be a hint CPU bottlenecks.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-cpu-wait"></a> vmware-esx-soap-host-cpu-wait

Check command object for the `check_vmware_esx` plugin. CPU time spent in wait state. The wait total includes time spent the CPU idle, CPU swap wait, and CPU I/O wait states. High or growing wait time can be a hint I/O bottlenecks.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-cpu-usage"></a> vmware-esx-soap-host-cpu-usage

Check command object for the `check_vmware_esx` plugin. Actively used CPU of the host, as a percentage of the total available CPU. Active CPU is approximately equal to the ratio of the used CPU to the available CPU.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. Defaults to "80%".
vmware_crit             | **Optional.** The critical threshold in percent. Defaults to "90%".


#### <a id="plugin-check-command-vmware-esx-soap-host-mem"></a> vmware-esx-soap-host-mem

Check command object for the `check_vmware_esx` plugin. All mem info(except overall and no thresholds).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-mem-usage"></a> vmware-esx-soap-host-mem-usage

Check command object for the `check_vmware_esx` plugin. Average mem usage in percentage.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. Defaults to "80%".
vmware_crit             | **Optional.** The critical threshold in percent. Defaults to "90%".


#### <a id="plugin-check-command-vmware-esx-soap-host-mem-consumed"></a> vmware-esx-soap-host-mem-consumed

Check command object for the `check_vmware_esx` plugin. Amount of machine memory used on the host. Consumed memory includes Includes memory used by the Service Console, the VMkernel vSphere services, plus the total consumed metrics for all running virtual machines in MB.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. No value defined as default.
vmware_crit             | **Optional.** The critical threshold in percent. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-mem-swapused"></a> vmware-esx-soap-host-mem-swapused

Check command object for the `check_vmware_esx` plugin. Amount of memory that is used by swap. Sum of memory swapped of all powered on VMs and vSphere services on the host in MB. In case of an error all VMs with their swap used will be displayed.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. No value defined as default.
vmware_crit             | **Optional.** The critical threshold in percent. No value defined as default.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-mem-overhead"></a> vmware-esx-soap-host-mem-overhead

Check command object for the `check_vmware_esx` plugin. Additional mem used by VM Server in MB.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. No value defined as default.
vmware_crit             | **Optional.** The critical threshold in percent. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-mem-memctl"></a> vmware-esx-soap-host-mem-memctl

Check command object for the `check_vmware_esx` plugin. The sum of all vmmemctl values in MB for all powered-on virtual machines, plus vSphere services on the host. If the balloon target value is greater than the balloon value, the VMkernel inflates the balloon, causing more virtual machine memory to be reclaimed. If the balloon target value is less than the balloon value, the VMkernel deflates the balloon, which allows the virtual machine to consume additional memory if needed.used by VM memory control driver. In case of an error all VMs with their vmmemctl values will be displayed.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in percent. No value defined as default.
vmware_crit             | **Optional.** The critical threshold in percent. No value defined as default.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-net"></a> vmware-esx-soap-host-net

Check command object for the `check_vmware_esx` plugin. Shows net info.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist NICs. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist expression as regexp.


#### <a id="plugin-check-command-vmware-esx-soap-host-net-usage"></a> vmware-esx-soap-host-net-usage

Check command object for the `check_vmware_esx` plugin. Overall network usage in KBps(Kilobytes per Second).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in KBps(Kilobytes per Second). No value defined as default.
vmware_crit             | **Optional.** The critical threshold in KBps(Kilobytes per Second). No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-net-receive"></a> vmware-esx-soap-host-net-receive

Check command object for the `check_vmware_esx` plugin. Data receive in KBps(Kilobytes per Second).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in KBps(Kilobytes per Second). No value defined as default.
vmware_crit             | **Optional.** The critical threshold in KBps(Kilobytes per Second). No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-net-send"></a> vmware-esx-soap-host-net-send

Check command object for the `check_vmware_esx` plugin. Data send in KBps(Kilobytes per Second).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold in KBps(Kilobytes per Second). No value defined as default.
vmware_crit             | **Optional.** The critical threshold in KBps(Kilobytes per Second). No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-net-nic"></a> vmware-esx-soap-host-net-nic

Check command object for the `check_vmware_esx` plugin. Check all active NICs.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist NICs. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist expression as regexp.


#### <a id="plugin-check-command-vmware-esx-soap-host-volumes"></a> vmware-esx-soap-host-volumes

Check command object for the `check_vmware_esx` plugin. Shows all datastore volumes info.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_subselect        | **Optional.** Volume name to be checked the free space.
vmware_gigabyte         | **Optional.** Output in GB instead of MB.
vmware_usedspace        | **Optional.** Output used space instead of free. Defaults to "false".
vmware_alertonly        | **Optional.** List only alerting volumes. Defaults to "false".
vmware_exclude          | **Optional.** Blacklist volumes name. No value defined as default.
vmware_include          | **Optional.** Whitelist volumes name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_warn             | **Optional.** The warning threshold for volumes. Defaults to "80%".
vmware_crit             | **Optional.** The critical threshold for volumes. Defaults to "90%".
vmware_spaceleft        | **Optional.** This has to be used in conjunction with thresholds as mentioned above.


#### <a id="plugin-check-command-vmware-esx-soap-host-io"></a> vmware-esx-soap-host-io

Check command object for the `check_vmware_esx` plugin. Shows all disk io info. Without subselect no thresholds can be given. All I/O values are aggregated from historical intervals over the past 24 hours with a 5 minute sample rate.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-io-aborted"></a> vmware-esx-soap-host-io-aborted

Check command object for the `check_vmware_esx` plugin. Number of aborted SCSI commands.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-resets"></a> vmware-esx-soap-host-io-resets

Check command object for the `check_vmware_esx` plugin. Number of SCSI bus resets.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-read"></a> vmware-esx-soap-host-io-read

Check command object for the `check_vmware_esx` plugin. Average number of kilobytes read from the disk each second.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-read-latency"></a> vmware-esx-soap-host-io-read-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) to process a SCSI read command issued from the Guest OS to the virtual machine.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-write"></a> vmware-esx-soap-host-io-write

Check command object for the `check_vmware_esx` plugin. Average number of kilobytes written to disk each second.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-write-latency"></a> vmware-esx-soap-host-io-write-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) taken to process a SCSI write command issued by the Guest OS to the virtual machine.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-usage"></a> vmware-esx-soap-host-io-usage

Check command object for the `check_vmware_esx` plugin. Aggregated disk I/O rate. For hosts, this metric includes the rates for all virtual machines running on the host.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-kernel-latency"></a> vmware-esx-soap-host-io-kernel-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) spent by VMkernel processing each SCSI command.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-device-latency"></a> vmware-esx-soap-host-io-device-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) to complete a SCSI command from the physical device.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-queue-latency"></a> vmware-esx-soap-host-io-queue-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) spent in the VMkernel queue.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-io-total-latency"></a> vmware-esx-soap-host-io-total-latency

Check command object for the `check_vmware_esx` plugin. Average amount of time (ms) taken during the collection interval to process a SCSI command issued by the guest OS to the virtual machine. The sum of kernelWriteLatency and deviceWriteLatency.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_warn             | **Optional.** The warning threshold. No value defined as default.
vmware_crit             | **Optional.** The critical threshold. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-media"></a> vmware-esx-soap-host-media

Check command object for the `check_vmware_esx` plugin. List vm's with attached host mounted media like cd,dvd or floppy drives. This is important for monitoring because a virtual machine with a mount cd or dvd drive can not be moved to another host.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist VMs name. No value defined as default.
vmware_include          | **Optional.** Whitelist VMs name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-service"></a> vmware-esx-soap-host-service

Check command object for the `check_vmware_esx` plugin. Shows host service info.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist services name. No value defined as default.
vmware_include          | **Optional.** Whitelist services name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime"></a> vmware-esx-soap-host-runtime

Check command object for the `check_vmware_esx` plugin. Shows runtime info: VMs, overall status, connection state, health, storagehealth, temperature and sensor are represented as one value and without thresholds.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-con"></a> vmware-esx-soap-host-runtime-con

Check command object for the `check_vmware_esx` plugin. Shows connection state.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-listvms"></a> vmware-esx-soap-host-runtime-listvms

Check command object for the `check_vmware_esx` plugin. List of VMware machines and their status.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist VMs name. No value defined as default.
vmware_include          | **Optional.** Whitelist VMs name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-status"></a> vmware-esx-soap-host-runtime-status

Check command object for the `check_vmware_esx` plugin. Overall object status (gray/green/red/yellow).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-health"></a> vmware-esx-soap-host-runtime-health

Check command object for the `check_vmware_esx` plugin. Checks cpu/storage/memory/sensor status.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist status name. No value defined as default.
vmware_include          | **Optional.** Whitelist status name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-health-listsensors"></a> vmware-esx-soap-host-runtime-health-listsensors

Check command object for the `check_vmware_esx` plugin. List all available sensors(use for listing purpose only).

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist status name. No value defined as default.
vmware_include          | **Optional.** Whitelist status name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-health-nostoragestatus"></a> vmware-esx-soap-host-runtime-health-nostoragestatus

Check command object for the `check_vmware_esx` plugin. This is to avoid a double alarm if you use **vmware-esx-soap-host-runtime-health** and **vmware-esx-soap-host-runtime-storagehealth**.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist status name. No value defined as default.
vmware_include          | **Optional.** Whitelist status name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-storagehealth"></a> vmware-esx-soap-host-runtime-storagehealth

Check command object for the `check_vmware_esx` plugin. Local storage status check.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist storage name. No value defined as default.
vmware_include          | **Optional.** Whitelist storage name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-temp"></a> vmware-esx-soap-host-runtime-temp

Check command object for the `check_vmware_esx` plugin. Lists all temperature sensors.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist sensor name. No value defined as default.
vmware_include          | **Optional.** Whitelist sensor name. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.


#### <a id="plugin-check-command-vmware-esx-soap-host-runtime-issues"></a> vmware-esx-soap-host-runtime-issues

Check command object for the `check_vmware_esx` plugin. Lists all configuration issues for the host.

Custom Attributes:



Name                    | Description
------------------------|--------------
vmware_host             | **Required.** ESX or ESXi hostname.
vmware_sslport          | **Optional.** SSL port connection. Defaults to "443".
vmware_ignoreunknown    | **Optional.** Sometimes 3 (unknown) is returned from a component. But the check itself is ok. With this option the plugin will return OK (0) instead of UNKNOWN (3). Defaults to "false".
vmware_ignorewarning    | **Optional.** Sometimes 2 (warning) is returned from a component. But the check itself is ok (from an operator view). With this option the plugin will return OK (0) instead of WARNING (1). Defaults to "false".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace.
vmware_sessionfile      | **Optional.** Session file name enhancement.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_nosession        | **Optional.** No auth session - IT SHOULD BE USED FOR TESTING PURPOSES ONLY!. Defaults to "false".
vmware_username         | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Required.** Use auth file instead username/password to session connect. No effect if **vmware_username** or **vmware_password** are defined <br> **Autentication file content:** <br>  username=vmuser <br> password=p@ssw0rd <br>  Defaults to "/etc/icinga2/vmware_esx_auth".
vmware_exclude          | **Optional.** Blacklist configuration issues. No value defined as default.
vmware_include          | **Optional.** Whitelist configuration issues. No value defined as default.
vmware_isregexp         | **Optional.** Treat blacklist and whitelist expressions as regexp.
vmware_multiline        | **Optional.** Multiline output in overview. This mean technically that a multiline output uses a HTML **\<br\>** for the GUI. No value defined as default.

Monitoring
==========

## <a id="plugin-check-commands"></a> Vmware
Icinga2 check commands for <a href="https://github.com/BaldMansMojo/check_vmware_esx"> vmware esx </a> plugins.

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
vmware_include          | **Optional.** Whitelist VM name. No value defined as default.
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

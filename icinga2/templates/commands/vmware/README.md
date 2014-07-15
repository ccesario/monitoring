Monitoring
==========

Icinga2 check commands for <a href="https://github.com/BaldMansMojo/check_vmware_esx"> vmware esx </a> plugins.

## <a id="plugin-check-commands"></a> Plugin Check Commands

#### <a id="plugin-check-command-vmware-esx-dc"></a> vmware esx dc

Check command object for the `check_vmware_esx` plugin.

Custom Attributes:


Name                    | Description
------------------------|--------------
vmware_trace            | **Optional.** Set verbosity level of vSphere API request/respond trace. Defauls to "0".
vmware_timeout          | **Optional.** Seconds before plugin times out. Defaults to "90".
vmware_ignorewarning    | **Optional.** Will return OK (0) instead of WARNING (1) when 2 (warning) are returned by a component. Defaults to "false". 
vmware_auth_nosession   | **Optional.** Don't use a session file for authentication. Defaults to "false".
vmware_sessionfile      | **Optional.** Vmware auth session file - no effect if **vmware_auth_nosession** is set. No value defined as default, the plugin will generate a random file.
vmware_sessionfiledir   | **Optional.** Path to store the **vmware_sessionfile** file. Defaults to "/var/spool/icinga2/tmp".
vmware_user             | **Optional.** The username to connect to Host or vCenter server. No value defined as default.
vmware_password         | **Optional.** The username's password. No value defined as default.
vmware_authfile         | **Optional.** Use auth file instead username/password to session connect. No effect if **vmware_user** or **vmware_password** are defined<br>
                                       **Autentication file content:** <br>
                                          username=<username> <br>
                                          password=<password> <br>
                                          Defaults to "/etc/icinga2/vmware_esx_auth".|


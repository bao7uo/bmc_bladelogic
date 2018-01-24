# BMC Bladelogic RSCD, change password, user list and remote execution
Exploiting vulnerabilities in BMC BladeLogic RSCD agent
- CVE-2016-1542 (BMC-2015-0010)
- CVE-2016-1543 (BMC-2015-0011)

This method of remote execution was achieved by doing my own research - it is performed using XMLRPC and has only been tested against Windows. The script will hang, but the command should execute.

![rexec poc](images/BMC_rexec.png)

Nick Bloor has a much better execution exploit using a different technique:
- https://github.com/NickstaDB/PoC/tree/master/BMC_RSCD_RCE
- https://nickbloor.co.uk/2018/01/01/rce-with-bmc-server-automation/
- https://nickbloor.co.uk/2018/01/08/improving-the-bmc-rscd-rce-exploit/
- https://www.tenable.com/plugins/index.php?view=single&id=91947

## Credits

BMC_getUsers and BMC_changePwd are modified from to https://github.com/ernw/insinuator-snippets/tree/master/bmc_bladelogic

I have added Windows compatibility to getUsers (change password in Windows should be possible with the rexec).

https://www.insinuator.net/2016/03/bmc-bladelogic-cve-2016-1542-and-cve-2016-1543/

Thanks to Nick Bloor for AWS image for testing.

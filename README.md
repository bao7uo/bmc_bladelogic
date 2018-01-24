Remote execution is performed using XMLRPC and has only been tested against Windows. The script will hang, but the command should execute.

BMC_getUsers and BMC_changePwd are modified from to https://github.com/ernw/insinuator-snippets/tree/master/bmc_bladelogic
I have added Windows version of getUsers.
Change password in windows should be possible with the rexec.

Exploiting CVE-2016-1542 (BMC-2015-0010) and CVE-2016-1543 (BMC-2015-0011) vulnerabilities in BMC BladeLogic RSCD agent.
Detailed information can be found here: https://www.insinuator.net/2016/03/bmc-bladelogic-cve-2016-1542-and-cve-2016-1543/

Use BMC_getUsers.py for user enumeration, and BMC_changePwd.py to change their passwords.

# deploying-app-in-ec2



touch .env
ls -al
vim .env
esc button
:wq to save and quit
:q to just quit


note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
ubuntu@ip-172-31-17-237:~/DataEngineerFAQ-s-App-using-BedRock$ sudo apt install python3-venv
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  python3-pip-whl python3-setuptools-whl python3.12-venv
The following NEW packages will be installed:
  python3-pip-whl python3-setuptools-whl python3-venv python3.12-venv
0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.
Need to get 2425 kB of archives.
After this operation, 2777 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 python3-pip-whl all 24.0+dfsg-1ubuntu1.1 [1703 kB]
Get:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 python3-setuptools-whl all 68.1.2-2ubuntu1.1 [716 kB]
Get:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 python3.12-venv amd64 3.12.3-1ubuntu0.3 [5678 B]
Get:4 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 python3-venv amd64 3.12.3-0ubuntu2 [1034 B]
Fetched 2425 kB in 0s (47.2 MB/s)      
Selecting previously unselected package python3-pip-whl.
(Reading database ... 108655 files and directories currently installed.)
Preparing to unpack .../python3-pip-whl_24.0+dfsg-1ubuntu1.1_all.deb ...
Unpacking python3-pip-whl (24.0+dfsg-1ubuntu1.1) ...
Selecting previously unselected package python3-setuptools-whl.
Preparing to unpack .../python3-setuptools-whl_68.1.2-2ubuntu1.1_all.deb ...
Unpacking python3-setuptools-whl (68.1.2-2ubuntu1.1) ...
Selecting previously unselected package python3.12-venv.
Preparing to unpack .../python3.12-venv_3.12.3-1ubuntu0.3_amd64.deb ...
Unpacking python3.12-venv (3.12.3-1ubuntu0.3) ...
Selecting previously unselected package python3-venv.
Preparing to unpack .../python3-venv_3.12.3-0ubuntu2_amd64.deb ...
Unpacking python3-venv (3.12.3-0ubuntu2) ...
Setting up python3-setuptools-whl (68.1.2-2ubuntu1.1) ...
Setting up python3-pip-whl (24.0+dfsg-1ubuntu1.1) ...
Setting up python3.12-venv (3.12.3-1ubuntu0.3) ...
Setting up python3-venv (3.12.3-0ubuntu2) ...
Scanning processes...                                                                                                                                                                                                     
Scanning candidates...                                                                                                                                                                                                    
Scanning linux images...                                                                                                                                                                                                  

Pending kernel upgrade!
Running kernel version:
  6.8.0-1016-aws
Diagnostics:
  The currently running kernel version is not the expected kernel version 6.8.0-1019-aws.

Restarting the system to load the new kernel will not be handled automatically, so you should consider rebooting.

Restarting services...

Service restarts being deferred:
 /etc/needrestart/restart.d/dbus.service
 systemctl restart networkd-dispatcher.service
 systemctl restart systemd-logind.service
 systemctl restart unattended-upgrades.service

No containers need to be restarted.

User sessions running outdated binaries:
 ubuntu @ session #1: sshd[1075]
 ubuntu @ user manager service: systemd[1422]

No VM guests are running outdated hypervisor (qemu) binaries on this host.
ubuntu@ip-172-31-17-237:~/DataEngineerFAQ-s-App-using-BedRock$ pyhton -m venv .venv
pyhton: command not found
ubuntu@ip-172-31-17-237:~/DataEngineerFAQ-s-App-using-BedRock$ pyhton3 -m venv .venv
Command 'pyhton3' not found, did you mean:
  command 'python3' from deb python3 (3.12.3-0ubuntu2)
Try: sudo apt install <deb name>
ubuntu@ip-172-31-17-237:~/DataEngineerFAQ-s-App-using-BedRock$ python3 -m venv .venv
ubuntu@ip-172-31-17-237:~/DataEngineerFAQ-s-App-using-BedRock$ source .venv/bin/activate

Target Communication Framework agent Debain Package
====================================================================================

Overview
------------------------------------------------------------------------------------

### Introduction

This is a repository for making tcf-agent(Target Communication Framework agent) debian package.

For details of tcf-agent, please refer to following URL.

  * git://git.eclipse.org/gitroot/tcf/org.eclipse.tcf.agent.git

Install
------------------------------------------------------------------------------------

### Download repository

```console
shell$ git clone --recursive --depth=1 -b 1.7.0-1 git://github.com/ikwzm/tcf-agent-dpkg
shell$ cd tcf-agent-dpkg
```

### Install Debian Package

```console
shell$ sudo apt install ./tcf-agent_1.7.0-1_arm64.deb 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Note, selecting 'tcf-agent' instead of './tcf-agent_1.7.0-1_arm64.deb'
The following NEW packages will be installed:
  tcf-agent
0 upgraded, 1 newly installed, 0 to remove and 69 not upgraded.
After this operation, 3,298 kB of additional disk space will be used.
Get:1 /home/fpga/work/tcf-agent-dpkg/tcf-agent_1.7.0-1_arm64.deb tcf-agent arm64 1.7.0-1 [689 kB]
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend will not work on a dumb terminal, an emacs shell buffer, or without a controlling terminal.)
debconf: falling back to frontend: Readline

Selecting previously unselected package tcf-agent.
(Reading database ... 114950 files and directories currently installed.)
Preparing to unpack .../tcf-agent_1.7.0-1_arm64.deb ...
Processing triggers for systemd (237-3ubuntu10.39) ...

```

### Start TCF-Agent

```console
shell$ sudo systemctl start tcf-agent.service
```

### Auto Start TCF-Agent

```console
shell$ sudo systemctl enable tcf-agent.service
```

### Stop TCF-Agent

```console
shell$ sudo systemctl stop tcf-agent.service
```

Build Debian Package
------------------------------------------------------------------------------------

### Download repository

```console
shell$ git clone --recursive --depth=1 -b 1.7.0-1 git://github.com/ikwzm/tcf-agent-dpkg
shell$ cd tcf-agent-dpkg
```

### Self Compile

```console
shell$ sudo debian/rules binary
    :
    :
    :
shell$ file tcf-agent_1.7.0-1_arm64.deb 
tcf-agent_1.7.0-1_arm64.deb: Debian binary package (format 2.0)
```

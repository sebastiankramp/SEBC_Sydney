# Preperation

## Swappiness
```bash
sudo sysctl -w vm.swappiness=1
```

## disable transparent hugepage compaction
```bash
never > defrag_file_pathname 
```

# Setup

## Cloudprovider
```
AWS 
```

## Nodes

|DNS external|IP external|IP internal|DNS internal|
|---|---|---|---|
|ec2-54-93-247-199.eu-central-1.compute.amazonaws.com|54.93.247.199|172.31.15.167|ip-172-31-15-167.eu-central-1.compute.internal
|ec2-54-93-248-62.eu-central-1.compute.amazonaws.com|54.93.248.62|172.31.11.170|ip-172-31-11-170.eu-central-1.compute.internal
|ec2-52-59-225-176.eu-central-1.compute.amazonaws.com|52.59.225.176|172.31.10.217|ip-172-31-10-217.eu-central-1.compute.internal
|ec2-35-158-118-178.eu-central-1.compute.amazonaws.com|35.158.118.178|172.31.3.122|ip-172-31-3-122.eu-central-1.compute.internal
|ec2-52-59-207-23.eu-central-1.compute.amazonaws.com|52.59.207.23|172.31.5.240|ip-172-31-5-240.eu-central-1.compute.internal


## Release
```bash
[root@ip-172-31-15-167 ec2-user]# cat /etc/*-release
NAME="Red Hat Enterprise Linux Server"
VERSION="7.2 (Maipo)"
ID="rhel"
ID_LIKE="fedora"
VERSION_ID="7.2"
PRETTY_NAME="Red Hat Enterprise Linux Server 7.2 (Maipo)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:redhat:enterprise_linux:7.2:GA:server"
HOME_URL="https://www.redhat.com/"
BUG_REPORT_URL="https://bugzilla.redhat.com/"

REDHAT_BUGZILLA_PRODUCT="Red Hat Enterprise Linux 7"
REDHAT_BUGZILLA_PRODUCT_VERSION=7.2
REDHAT_SUPPORT_PRODUCT="Red Hat Enterprise Linux"
REDHAT_SUPPORT_PRODUCT_VERSION="7.2"
Red Hat Enterprise Linux Server release 7.2 (Maipo)
Red Hat Enterprise Linux Server release 7.2 (Maipo)
```

## Disk capacity
```bash
[root@ip-172-31-15-167 ec2-user]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       30G  927M   30G   4% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   17M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/1000

```

## Repolist
```bash
[root@ip-172-31-15-167 ec2-user]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
rhui-REGION-client-config-server-7                                                                                                                                                                   | 2.9 kB  00:00:00
rhui-REGION-rhel-server-releases                                                                                                                                                                     | 3.5 kB  00:00:00
rhui-REGION-rhel-server-rh-common                                                                                                                                                                    | 3.8 kB  00:00:00
(1/7): rhui-REGION-rhel-server-releases/7Server/x86_64/updateinfo                                                                                                                                    | 1.9 MB  00:00:00
(2/7): rhui-REGION-client-config-server-7/x86_64/primary_db                                                                                                                                          | 4.3 kB  00:00:00
(3/7): rhui-REGION-rhel-server-releases/7Server/x86_64/group                                                                                                                                         | 701 kB  00:00:00
(4/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/group                                                                                                                                        |  104 B  00:00:00
(5/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/updateinfo                                                                                                                                   |  33 kB  00:00:00
(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/primary_db                                                                                                                                   | 118 kB  00:00:00
(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/primary_db                                                                                                                                    |  35 MB  00:00:00
repo id                                                                                            repo name                                                                                                          status
rhui-REGION-client-config-server-7/x86_64                                                          Red Hat Update Infrastructure 2.0 Client Configuration Server 7                                                         4
rhui-REGION-rhel-server-releases/7Server/x86_64                                                    Red Hat Enterprise Linux Server 7 (RPMs)                                                                           14,277
rhui-REGION-rhel-server-rh-common/7Server/x86_64                                                   Red Hat Enterprise Linux Server 7 RH Common (RPMs)                                                                    228
repolist: 14,509
```

## adding users and groups
```bash
[root@ip-172-31-10-217 ec2-user]# groupadd kiwis
[root@ip-172-31-10-217 ec2-user]# groupadd aussies
[root@ip-172-31-10-217 ec2-user]# useradd -u 2300 -g aussies cate
[root@ip-172-31-10-217 ec2-user]# useradd -u 2900 -g kiwis jemaine
[root@ip-172-31-10-217 ec2-user]# cat /etc/passwd | grep cate
cate:x:2300:1002::/home/cate:/bin/bash
[root@ip-172-31-10-217 ec2-user]# cat /etc/passwd | grep jemaine
jemaine:x:2900:1001::/home/jemaine:/bin/bash
[root@ip-172-31-10-217 ec2-user]# cat /etc/group | grep aussies
aussies:x:1002:
[root@ip-172-31-10-217 ec2-user]# cat /etc/group | grep kiwis
kiwis:x:1001:
```





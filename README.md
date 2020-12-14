ShadowsocksR
===========

[![Build Status]][Travis CI]  [[中文]]

A fast tunnel proxy that helps you bypass firewalls.

Usage
------

### Clone or download project

``` text
~ $ git clone https://github.com/showzeng/shadowsocksr
```

### Usage for single user on linux platform

Fill in your configuration file (shadowsocksr/config.json):

``` json
{
    "server": "0.0.0.0",
    "server_ipv6": "::",
    "server_port": 8388,
    "local_address": "127.0.0.1",
    "local_port": 1080,

    "password": "m",
    "method": "aes-128-ctr",
    "protocol": "auth_aes128_md5",
    "protocol_param": "",
    "obfs": "tls1.2_ticket_auth_compatible",
    "obfs_param": "",
    "speed_limit_per_con": 0,
    "speed_limit_per_user": 0,

    "additional_ports" : {},
    "additional_ports_only" : false,
    "timeout": 120,
    "udp_timeout": 60,
    "dns_ipv6": false,
    "connect_verbose_info": 0,
    "redirect": "",
    "fast_open": false
}
```

You need config your configuration with these items:

``` json
{
    "server": "0.0.0.0",
    "server_port": 8388,

    "password": "m",
    "method": "aes-128-ctr",
    "protocol": "auth_aes128_md5",
    "obfs": "tls1.2_ticket_auth_compatible",
}
```

Then turn on your terminal and get into "shadowsocksr/" folder. Excute the command as below:

``` text
~/shadowsocksr [manyuser] $ chmod 755 runssr stopssr

~/shadowsocksr [manyuser] $ sudo mv runssr stopssr /usr/local/bin
[sudo] password for xxxx: 

~/shadowsocksr [manyuser] $ ../

~ $ sudo mv shadowsocksr/ /opt/

~ $ source /etc/profile
```

Once done with that, you can turn on/off shadowsocksR with these simple command at anytime as you wish :p , such as you just open your computer.

### Turn on SSR

``` text
~ $ runssr
```

### Turn off SSR

``` text
~ $ stopssr
```

Documentation
-------------

You can find all the documentation in the [Wiki].

License
-------

Copyright 2015 clowwindy

Licensed under the Apache License, Version 2.0 (the "License"); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.

Bugs and Issues
----------------

* [Issue Tracker]


[Build Status]:      https://travis-ci.org/shadowsocksr/shadowsocksr.svg?branch=manyuser
[Travis CI]:         https://travis-ci.org/shadowsocksr/shadowsocksr
[Wiki]:              https://github.com/breakwa11/shadowsocks-rss/wiki
[Issue Tracker]:     https://github.com/shadowsocksr/shadowsocksr/issues?state=open
[中文]:               https://showzeng.itscoder.com/linux/2017/12/02/use-ssr-under-linux.html

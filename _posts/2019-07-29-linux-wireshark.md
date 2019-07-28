---
layout: post
title: ubuntu下wireshark权限问题
tags: ['linux','ubuntu', 'wireshark']
---

解决wireshark在ubuntu下需要root权限的问题



- 创建wireshark用户组

    ```bash
    sudo gruopadd wireshark
    ```

    

- 把dumpcap的用户组修改为wireshark

    ```bash
    sudo chgrp wireshark /usr/bin/dumpcap
    ```

    

- 让wireshark用户组有root权限使用***dumpcap***

    ```bash
    sudo chmod 4755 /usr/bin/dumpcap
    ```

    

- 把当前用户的加入到wireshark用户组

    ```bash
    sudo gpasswd -a <userId> wireshark
    ```

    

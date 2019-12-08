---
layout: post
title: Install MariaDB on Manjaro
tags: ['linux','manjaro', 'mariadb']
---

# Install MariaDB on Manjaro
* Install mariadb binary package
    ```bash
        sudo pacman -Syv mariadb
    ```
* Initialize database
    ```bash
        sudo mysql_install_db --user=mysql --basedir=/usr --datadar=/var/lib/mysql
    ```
* Start mariadb
    ```bash
        systemctl start mariadb
    ```
* Change the password
```bash
    /us/bin/mysql_secure_installation
```

* Enable/Disable the auto start-up

    * Enable auto startup
    ```bash
        sudo systemctl enable mariadb
    ```
    * Disable auto startup
    ```bash
        sudo systemctl disable mariadb
    ```

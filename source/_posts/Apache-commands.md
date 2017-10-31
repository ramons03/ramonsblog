title: Apache commands
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-14 10:07:20
tags:
---
###  Working with apache on Centos.


* Install apache
  ```sh
  sudo yum install httpd
  ```
* Start Apache. [apachectl](https://httpd.apache.org/docs/2.4/programs/apachectl.html)
  ```sh
  sudo systemctl start httpd.service
  ```
  * Check where is installed
    ```sh
    whereis httpd
    ```
  * Check apache status
    ```sh
    sudo systemctl status httpd
    ```
  * Start apache on boot
    ```sh
    sudo systemctl enable httpd.service
    ```
  * Stop apache
    ```sh
    sudo systemctl stop httpd
    ```
  * Restart apache
    ```sh
    sudo systemctl restart httpd.service
    ```
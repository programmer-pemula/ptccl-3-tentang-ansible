﻿﻿﻿﻿﻿ANSIBLE
-----------

## **Tentang Ansible**
_Ansible_ adalah sebuah provisioning tool yang dikembangkan oleh RedHat. Dimana kamu dapat mencatat setiap proses deployment ataupun konfigurasi yang biasa dilakukan berulang - ulang terhadap beberapa server.

## Langkah Penggunaan (katakoda)
### Ansible - Configuring CentOS with Ansible
``echo "[group1]" > myhosts && \ echo "host01 ansible_ssh_user=cent" >> myhosts
``

``ansible group1 -i myhosts -m command -a date``

![langkah 1](images/ansible-centos-1.png)

### Ansible Configuring CentOS with Ansible part 1

![langkah 2](images/ansible-centos-2.png)

### Ansible Configuring CentOS with Ansible part 2

![langkah 3](images/ansible-centos-3.png)

### Ansible Configuring CentOS with Ansible part 3




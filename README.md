# Задание 8.3

В site.yaml добавлены Play "Install nginx" и "Install lighthouse" 

В inventory добавлена группа хостов lighthouse

В templates добавлен шаблон конфига nginx.conf.j2



```
mikhail@Ubuntu1:/8.3/ansible8.3$ ansible-playbook site.yml -i inventory/prod.yml

PLAY [Install Clickhouse] *******************************************************************************************************************

TASK [Get clickhouse] ***********************************************************************************************************************
ok: [clickhouse-01]

TASK [Install clickhouse packages] **********************************************************************************************************
ok: [clickhouse-01]

TASK [Create database] **********************************************************************************************************************
ok: [clickhouse-01]

PLAY [Install Vector] ***********************************************************************************************************************

TASK [Get vector rpm] ***********************************************************************************************************************
ok: [vector-01]

TASK [Install vector rpm] *******************************************************************************************************************
ok: [vector-01]

PLAY [Install nginx] ************************************************************************************************************************

TASK [NGINX - Add repository] ***************************************************************************************************************
ok: [lighthouse-01]

TASK [NGINX - Install] **********************************************************************************************************************
ok: [lighthouse-01]

TASK [NGINX - create config] ****************************************************************************************************************
ok: [lighthouse-01]

PLAY [Install lighthouse] *******************************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************************************
ok: [lighthouse-01]

TASK [Install dependencies] *****************************************************************************************************************
ok: [lighthouse-01]

TASK [Lighthouse - install] *****************************************************************************************************************
ok: [lighthouse-01]

PLAY RECAP **********************************************************************************************************************************
clickhouse-01              : ok=3    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
lighthouse-01              : ok=6    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
vector-01                  : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```

![img.png](img.png)

#### VM с lighthouse ####
![img_1.png](img_1.png)
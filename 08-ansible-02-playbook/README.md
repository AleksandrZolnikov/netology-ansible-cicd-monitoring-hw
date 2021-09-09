### Подготовьте README.md файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.  
Плейбук разворачивает Elasticsearch и Kibana на docker контейнерах.  
Теги плейбука:
```
# ansible-playbook site.yml --list-tags
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'
[WARNING]: Could not match supplied host pattern, ignoring: elasticsearch
[WARNING]: Could not match supplied host pattern, ignoring: kibana

playbook: site.yml

  play #1 (all): Install Java   TAGS: []
      TASK TAGS: [java]

  play #2 (elasticsearch): Install Elasticsearch        TAGS: []
      TASK TAGS: [elastic]

  play #3 (kibana): Install Kibana      TAGS: []
      TASK TAGS: [kibana]
  ```
  all - таски для всех хостов.  
  elasticsearch - таски для установки elasticsearch.  
  kibana - таски для установки kibana.  
  Переменные плейбука:  
  java_jdk_version - версия java. (11.0.12).   
  java_oracle_jdk_package - файл для установки(имя). ("jdk-{{ java_jdk_version }}_linux-x64_bin.tar.gz")  
  java_home - директория, куда устанавливаем java. ("/opt/jdk/{{ java_jdk_version }}")  
  elastic_version - версия ES для установки. (7.10.1)  
  elastic_home - директория для установки ES. ("/opt/elastic/{{ elastic_version }}")  
  kibana_version - версия kibana для установки. (7.14.1)  
  kibana_home - директория для установки kibana. ("/opt/kibana/{{ kibana_version }}")  
  

###  Домашнее задание к занятию "8.4 Работа с Roles"
Машины в облаке разворачиваются terraform-ом, также им заполняется файл hosts.yml, и на машины  
добавляется пользователь и ключ, для работы ansible.  
Файлы для развертывания прилагаются.  
Токен прописываем в строке запуска:  
```
terraform apply -var="token=....."  
### Hostname
---
Чтобы поменять имя устройства необходимо зайти в режим конфигурации и написать следующее:

```
Switch# conf t
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)#
```

> Чтобы удалить настроенное имя узла и вернуть стандартный диалог командной строки для коммутатора, используйте команду глобальной конфигурации `no hostname`

### Пользовательский режим EXEC
---
```
Sw-Floor-1# conf t
Sw-Floor-1(config)# line console 0
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

> cisco - это ваш пароль

### Привилегированный режим EXEC
---
```
Sw-Floor-1# conf t
Sw-Floor-1(config)# enable secret class
Sw-Floor-1(config)# exit
Sw-Floor-1#
```

> class - это ваш пароль

### Линии виртуального терминала (VTY)
---
```
Sw-Floor-1# conf t
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

> cisco - это ваш пароль

### Шифрование паролей
---
```
Sw-Floor-1# conf t
Sw-Floor-1(config)# service password-encryption
```

### Баннерные сообщения
---
```
Sw-Floor-1# conf t
Sw-Floor-1(config)# banner motd #Authorized Access Only#
```

### Файлы конфигурации
---
Для сохранения настроек необходимо выполнить команду:
```
copy running-config startup-config
```
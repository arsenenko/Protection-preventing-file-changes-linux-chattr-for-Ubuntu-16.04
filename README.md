# Protection preventing file changes linux chattr Ubuntu-16.04
<a href="https://ibb.co/hSHFZJ"><img src="https://preview.ibb.co/eboNEJ/chattr_command_tech_tutorials.jpg" alt="chattr_command_tech_tutorials" border="0"></a><br /><a target='_blank' ></a><br />

Данная  команда может изменять атрибуты файлов, Linux запреты на удаления файлов или изменения и даже из под правами суперпользователя /root.
---
Chattr - поддерживает файловые системы как (ReiserFS.XFS.Btrfs ext2.ext3.ext4)......
---
# Структура синтаксиса команд:

1. chattr - (Изменения Атрибутов) 

2. lsattr - (Просмотр Атрибутов)

# chattr [-RVf] [Оператор][атрибуты] /файл

[ Оператор ] :

“+” - Добаваить 
“-” - Удалить 
“=” - Перезаписать 
“-R +i” - Папка 

# [ Пример атрибутов ]

“a” - Только редактировать в режиме добавления 

“A” - не обновлять время перезаписи 

“c” - авто.сжать при записи на диск 

“C” -Отек. копирования при записи 

“i” - сделать не известным …. 

# Пример 1

В данном примере мы будем менять атрибут файла /etc/passwd 

и после изменения его атрибутов не будет возможности его редактировать или удалять даже суперпользователю root …..

# sudo chattr +i /etc/passwd  
(запрет и модификация атрибута файла )

# sudo lsattr /etc/passwd 
(Просмотр состояния атрибутов файлов )

# Вернуть исходное состояния файла  

#sudo chattr -i /etc/passwd 

<a href="https://ibb.co/i0zLZJ"><img src="https://preview.ibb.co/g4FuuJ/16152651317_076a65cf50_b.jpg" alt="16152651317_076a65cf50_b" border="0"></a><br />
Пример 2



# sudo chattr +a /var/log/syslog 
(Атрибуты только на добавления )


# containers02 
## Запуск и тестирование
Открываю терминал в папке containers03 и выполняю команду:
`docker build -t containers03 .`

Образ создавался около 10ти секунд.

Затем запускаю контейнер:
`docker run -it --name containers02 containers03`

Согласно синтасису Dokerfile (CMD - Задаёт команду, которая будет выполнена при запуске контейнера.) при запуске контейнера вывелось *hello from "my hostname"*

Удаляю контейнер и запускаю снова, выполнив команды:
```
docker rm containers03
docker run -ti --name containers03 containers03 bash
```

В открывшемся окне выполните команды:
```
cd /var/www/html/
ls -l
```
Вывод команды ls -l: 
total 4
-rwxr-xr-x 1 root root 238 Feb 28 12:01 index.html

Команда ls -l выводит детальную информацию о файлах и папках в каталоге, права доступа, владелец файла, дата и время последнего использования и его имя




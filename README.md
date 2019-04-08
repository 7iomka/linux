# linux
Действия в линуксе


1) Отрубил службу ожидания онлайн-подключения (возможны траблы и задержки в запуске прог которым она нужна) `sudo systemctl disable NetworkManager-wait-online.service`
2) Перевёл линукс на местное время как в винде - `timedatectl set-local-rtc 1` (чтобы вернуть как было надо сделать `timedatectl set-local-rtc 0`)
3) Исправляем фризы - https://easylinuxtipsproject.blogspot.com/p/bugs.html#ID25
4) после установки новой версии docker-compose - чистим хэш `has -r`
5) исправляем ошибку `System limit for number of file watchers reached, watch` командой `echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p`

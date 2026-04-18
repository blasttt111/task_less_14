# Написать скрипт для мониторинга systemd-службы 
  - имя службы задается через позиционный аргумент
  - проверяется налилчие указанной в аргументе службы
  - если она существует - раз в минуту проверяется работает она или нет
  - если НЕ работатет - производится попытка запустить службу (3 попытки с интервалом 5 секунд)
  - после каждой попытки проверяет, запустилась сулжба или нет
  - все действия логируются в файл `checker.log` в заданном формате
  - написать systemd unit для запуска скрипта как systemd-службы
<img width="963" height="562" alt="image" src="https://github.com/user-attachments/assets/9fec038b-a5bc-4117-89fe-348ba9c59717" />

<img width="1153" height="612" alt="image" src="https://github.com/user-attachments/assets/6df18163-a1ad-44eb-8029-094f3489ff3c" />

  - напишем unit файл

<img width="796" height="323" alt="image" src="https://github.com/user-attachments/assets/e9e64312-a853-4d69-8e6c-5a91ebe8b2f4" />

  - остановим nginx, проверим что служба `checker.service` работает

<img width="974" height="274" alt="image" src="https://github.com/user-attachments/assets/89f9590d-6d37-4fbf-a67c-532b2a66c5e1" />

  - остановил Nginx, скрипт сразу его перезапустил

<img width="1295" height="738" alt="image" src="https://github.com/user-attachments/assets/f1a087dd-fad8-43aa-bd33-b195e8b29ff5" />

# Написать скрипт для управления приложения simple-server
  - запуск процесса в фоновом режиме с перенаправлением stdout и stderr в файл simple-server.log
  - остановка процесса
  - проверка работоспособности приложения (curl)
  - все действия логируются в файл simple-server-control.log

<img width="1015" height="669" alt="image" src="https://github.com/user-attachments/assets/5ea61b3f-748f-4505-a869-fb542728de71" />

<img width="1023" height="674" alt="image" src="https://github.com/user-attachments/assets/dedbb1b3-b6c8-436e-8a3b-7a20e3eccc27" />

  - проверка

<img width="819" height="687" alt="image" src="https://github.com/user-attachments/assets/12e8bd6c-cce2-474c-bc0c-4f98f7c8b53c" />

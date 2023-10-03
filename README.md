# SIEM_pr1
Установим 2 копии дистрибутива Debian 12.

IP адрес первого хоста: 192.168.135.132.
 ![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/c89f669e-b5f5-42be-bada-9754ee441de3)

IP адрес второго хоста: 192.168.135.133.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/b76f4d4a-ffce-4935-be89-babbf2860fb1)

 
Проверим сетевую доступность между хостами при помощи утилиты “ping”.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/1422d365-184c-4d7c-ad87-54a43331c6a2)

 
2-ю ВМ сделаем сервером. Для этого установим на нее rsyslog.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/4a430066-d4cd-4c91-9c6a-9855806f8cb4)

 
Запустим работу rsyslog.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/10ca1608-ea8c-4e58-81d9-a374bd0bb631)

 
Настроим rsyslog в качестве центрального сервера журналирования, установим протокол TCP для удаленного приема системных журналов и порт 514 для прослушивания. А также определим набор правил для обработки журналов.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/af47c68c-eb60-4a51-b9be-2ecf947f6194)

 
Проверим сетевые сокеты rsyslog.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/ca7becb2-c98d-4f7c-a6fb-913603396a8b)

 
Теперь установим и запустим rsyslog на клиентской ВМ.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/52b2ef83-738c-4e96-9d33-5bff26a8e647)

 
Настроим отправку журналов с клиента.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/61539109-9600-443b-a2f7-09562a7a41a3)

 
Перезапустим демон rsyslog на клиентской ВМ.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/19f3c839-e4a6-4a74-a7b5-b8aef3915fc5)

Проверим, действительно ли rsyslog получает и регистрирует сообщения от клиента.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/9c6b4e4b-0868-46da-bbbd-7927caab2e64)

Затем установим и настроим Loki.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/5f090672-5700-4860-980a-b603cd6e41a7)
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/e5e2fc02-e905-4a49-a673-6cb87cf9015a)
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/22c8abca-118a-4c9c-940f-db205c719c18)

После чего установим Promtail.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/2d3ef3c9-57e0-495b-a54a-84ae3088e958)
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/862e811f-5b3f-4f0a-801f-61b9bba68ee0)
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/3cb596f8-3d94-483d-8423-5b93e905dfad)

И затем установим SigNoz.
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/0eff465b-342b-4286-80c3-5cb3fceeb8b7)
![image](https://github.com/ivan7447/SIEM_pr1/assets/137392628/99b28592-e49d-4c99-abd6-05f4c7800afa)

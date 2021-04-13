---
title: Bluetooth и подключение
description: Bluetooth использует функцию Connect для подключения к целевому устройству Bluetooth с помощью ранее созданного сокета Bluetooth.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- подключение Bluetooth
- Bluetooth и подключение Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488193"
---
# <a name="bluetooth-and-connect"></a>Bluetooth и подключение

Bluetooth использует функцию [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) для подключения к целевому устройству Bluetooth с помощью ранее созданного сокета Bluetooth. Параметр *Name* функции **Connect** , который является структурой [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , должен указывать целевое устройство Bluetooth. Для определения целевого устройства используются два механизма:

-   Структура [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) может напрямую указывать номер порта, к которому запрашивается соединение. Этот механизм требует, чтобы приложение выполняло собственные запросы SDP перед попыткой выполнить операцию [**подключения**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   Структура [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) может указывать уникальный идентификатор класса службы, к которому требуется подключиться. Если у однорангового устройства несколько портов, соответствующих ИДЕНТИФИКАТОРу класса службы, вызов функции [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) подключается к первой допустимой службе. Этот механизм можно использовать без предыдущих запросов SDP.

При использовании структуры [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) с функцией [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) применяются следующие требования.

-   Элемент **бтаддр** должен быть допустимым адресом удаленного радиоприемника.
-   Для члена **сервицеклассид** , если элемент порта равен нулю, система пытается использовать **сервицеклассид** для разрешения удаленного порта, соответствующего службе. Класс службы — это нормализованный 128-разрядный идентификатор GUID, определяемый спецификацией Bluetooth. Общие идентификаторы GUID определяются документом с назначенными номерами Bluetooth. Кроме того, для доменного приложения можно использовать уникальный идентификатор GUID.
-   Элемент **порта** должен быть допустимым удаленным портом или равняться нулю, если указан член **сервицеклассид** .

В следующей таблице перечислены коды результатов для Bluetooth и функции [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Ошибка/Ошибка\#                    | Описание                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Функция [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , вызываемая для уже подключенного сокета. |
| WSAEACCES10013<br/>        | Выполняется подключение к запрошенному приложению Аутентификация, но проверка подлинности не удалась.        |
| WSAENOBUFS10055<br/>       | Неустранимая ошибка нехватки памяти.                                                 |
| WSAEADDRINUSE10048<br/>    | Запрошенный номер порта/канала уже используется.                                       |
| WSAETIMEDOUT10060<br/>     | Время ожидания ввода-вывода истекло на радиочастоте Bluetooth ( \_ время ожидания страницы).                    |
| WSAEDISCON10101<br/>       | Канал RFCOMM отключен удаленным одноранговым узлом.                                    |
| WSAECONNRESET10054<br/>    | Мультиплексор RFCOMM (сеанс) отключен удаленным одноранговым узлом.                      |
| WSAECONNABORTED10053<br/>  | Завершение работы сокета приложением.                                                   |
| WSAENETUNREACH10051<br/>   | Ошибка, отличная от времени ожидания на уровне L2CAP или Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | RFCOMM получил ответ DM.                                                   |
| WSAENETDOWN10050<br/>      | Непредвиденная сетевая ошибка.                                                          |
| WSAESHUTDOWN10058<br/>     | Канал L2CAP отключен удаленным одноранговым узлом.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Недопустимый порт или канал Bluetooth или адрес устройства.                                |
| WSAEINVAL10022<br/>        | Самонастраивающийся, событие с стеком драйвера или другая ошибка привела к сбою.                  |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**соединиться**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 


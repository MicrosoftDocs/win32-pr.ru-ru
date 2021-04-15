---
title: Программирование Bluetooth с помощью сокетов Windows
description: В этом разделе описывается, как использовать функции и структуры сокетов Windows для программирования приложения Bluetooth.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, задачи
- Сокеты Windows
- программирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654317"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Программирование Bluetooth с помощью сокетов Windows

В этом разделе описывается, как использовать функции и структуры сокетов Windows для программирования приложения Bluetooth. Полные справочные сведения о элементах API сокетов Windows можно найти в [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2). в этом разделе приводятся только сведения, относящиеся к Bluetooth, для каждого элемента программирования Windows Sockets.

Вы также можете скачать [Пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) для получения полного примера.

Как и при программировании всех приложений Windows Sockets, функция [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) должна быть вызвана для инициации функций сокетов Windows и включения Bluetooth.

В следующих разделах приводятся рекомендации по использованию функций и структур Windows Sockets с API Microsoft Bluetooth.



| Раздел                                                                                            | Описание                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth и Accept](bluetooth-and-accept.md)                                                 | Bluetooth использует функцию [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) для включения входящих попыток подключения к сокету.<br/>                                                                                                                                                                                                  |
| [Bluetooth и привязка](bluetooth-and-bind.md)                                                     | Bluetooth использует функцию [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) для привязки к сокету.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth и большой двоичный объект](bluetooth-and-blob.md)                                                     | Bluetooth использует структуру [**больших двоичных объектов**](/windows/desktop/api/nspapi/ns-nspapi-blob) для передачи или получения данных, относящихся к транспорту, в структуру [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) во время вызовов функций [**всасетсервице**](bluetooth-and-wsasetservice.md) или **всалукупсервице** \* . <br/>             |
| [Bluetooth и подключение](bluetooth-and-connect.md)                                               | Bluetooth использует функцию [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) для подключения к целевому устройству Bluetooth с помощью ранее созданного сокета Bluetooth.<br/>                                                                                                                                                              |
| [Bluetooth и функцию getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | Функция [**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов.<br/>                                                                                                                                                                                   |
| [Bluetooth и жетпирнаме](bluetooth-and-getpeername.md)                                       | Используется для получения адреса Bluetooth однорангового устройства Bluetooth.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth и жетсоккнаме](bluetooth-and-getsockname.md)                                       | Bluetooth использует функцию [**жетсоккнаме**](/windows/desktop/api/winsock/nf-winsock-getsockname) для получения адреса и номера порта серверного устройства, выделенного сокету посредством предыдущего вызова функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth и жетсоккопт](bluetooth-and-getsockopt.md)                                         | Bluetooth использует функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) для запроса различных параметров, связанных с каналом сервера или соединением. <br/>                                                                                                                                                           |
| [Bluetooth и прослушивание, выбор и функции closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth использует функции [**прослушивания**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**выбора**](/windows/desktop/api/winsock2/nf-winsock2-select)и [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) без каких бы то ни было изменений в стандартном программировании Windows Sockets.<br/>                                                                                                   |
| [Bluetooth, операции чтения или записи](bluetooth-and-read-or-write-operations.md)             | Сведения о поддерживаемых операциях чтения и записи Winsock.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth и сетсоккопт](bluetooth-and-setsockopt.md)                                         | Bluetooth использует функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для установки различных параметров, связанных с каналом сервера или соединением.<br/>                                                                                                                                                              |
| [Bluetooth и завершение работы](bluetooth-and-shutdown.md)                                             | Bluetooth использует функцию [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) для отключения от удаленного радио.<br/>                                                                                                                                                                                                             |
| [Bluetooth и сокет](bluetooth-and-socket.md)                                                 | Bluetooth использует функцию [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) для создания сокета для входящих или исходящих соединений.<br/>                                                                                                                                                                                               |
| [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md)                                 | Сведения о параметрах сокета, поддерживаемых Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth и Всааддресстостринг](bluetooth-and-wsaaddresstostring.md)                         | Используется для преобразования адреса устройства Bluetooth в строку, которая, в свою очередь, предоставляется функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) через структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) при получении сведений о службе устройства.<br/>                                           |
| [Bluetooth и Всалукупсервицебегин](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth использует функцию [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запроса устройств и обнаружения служб.<br/>                                                                                                                                                                         |
| [Bluetooth и Всалукупсервиценекст](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth использует функцию [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) для сопоставления запросов, указанных в предыдущем вызове функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth и Всалукупсервицеенд](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth использует функцию [**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) для завершения запроса, инициированного в предыдущем вызове [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), и, возможно, расширен в последующих вызовах [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth и ВСАКУЕРИСЕТ](bluetooth-and-wsaqueryset.md)                                       | Структура [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) используется в операциях, включая запрос устройства, запрос службы и настройку службы.<br/>                                                                                                                                                                |
| [Bluetooth и Всасетсервице](bluetooth-and-wsasetservice.md)                                   | Bluetooth использует функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ БС) из реестра.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 


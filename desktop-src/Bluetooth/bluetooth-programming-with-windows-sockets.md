---
title: Bluetooth программирование с помощью сокетов Windows
description: в этом разделе описано, как использовать функции и структуры сокетов Windows для программирования Bluetooth приложения.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, задачи
- Сокеты Windows
- программирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004094"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth программирование с помощью сокетов Windows

в этом разделе описано, как использовать функции и структуры сокетов Windows для программирования Bluetooth приложения. полные справочные сведения об элементах API Windows sockets можно найти в [Windowsных сокетах](/windows/desktop/WinSock/windows-sockets-start-page-2). в этом разделе приводятся сведения только о Bluetooth для каждого элемента программирования Windowsных сокетов.

вы также можете скачать [пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) для получения полного примера.

как и при программировании всех Windows сокетов, необходимо вызвать функцию [**сбой wsastartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) , чтобы инициировать функции Windowsных сокетов и включить Bluetooth.

в следующих разделах приводятся рекомендации по использованию функций и структур Windows сокетов с помощью Microsoft Bluetooth API:



| Раздел                                                                                            | Описание                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth и принять](bluetooth-and-accept.md)                                                 | Bluetooth использует функцию [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) для включения входящих попыток подключения к сокету.<br/>                                                                                                                                                                                                  |
| [Bluetooth и bind](bluetooth-and-bind.md)                                                     | Bluetooth использует функцию [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) для привязки к сокету.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth и BLOB-объект](bluetooth-and-blob.md)                                                     | Bluetooth использует структуру [**больших двоичных объектов**](/windows/desktop/api/nspapi/ns-nspapi-blob) для передачи или получения данных, относящихся к транспорту, в структуру [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) во время вызовов функций [**всасетсервице**](bluetooth-and-wsasetservice.md) или **всалукупсервице** \* . <br/>             |
| [Bluetooth и подключение](bluetooth-and-connect.md)                                               | Bluetooth использует функцию [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) для подключения к целевому устройству Bluetooth, используя ранее созданный сокет Bluetooth.<br/>                                                                                                                                                              |
| [Bluetooth и функцию getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | Функция [**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов.<br/>                                                                                                                                                                                   |
| [Bluetooth и жетпирнаме](bluetooth-and-getpeername.md)                                       | используется для получения адреса Bluetooth однорангового Bluetooth устройства.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth и жетсоккнаме](bluetooth-and-getsockname.md)                                       | Bluetooth использует функцию [**жетсоккнаме**](/windows/desktop/api/winsock/nf-winsock-getsockname) для получения адреса устройства сервера и номера порта, выделенного сокету через предыдущий вызов функции [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth и жетсоккопт](bluetooth-and-getsockopt.md)                                         | Bluetooth использует функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) для запроса различных параметров, связанных с каналом сервера или соединением. <br/>                                                                                                                                                           |
| [Bluetooth и прослушивание, выбор и функции closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth использует функции [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)и [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) без каких бы то ни было изменений в стандартном программировании Windowsных сокетов.<br/>                                                                                                   |
| [Bluetooth и операции чтения или записи](bluetooth-and-read-or-write-operations.md)             | Сведения о поддерживаемых операциях чтения и записи Winsock.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth и сетсоккопт](bluetooth-and-setsockopt.md)                                         | Bluetooth использует функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для установки различных параметров, связанных с каналом сервера или соединением.<br/>                                                                                                                                                              |
| [Bluetooth и завершение работы](bluetooth-and-shutdown.md)                                             | Bluetooth использует функцию [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) для отключения от удаленного радио.<br/>                                                                                                                                                                                                             |
| [Bluetooth и сокет](bluetooth-and-socket.md)                                                 | Bluetooth использует функцию [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , создает сокет для входящих или исходящих соединений.<br/>                                                                                                                                                                                               |
| [параметры Bluetooth и сокетов](bluetooth-and-socket-options.md)                                 | Сведения о параметрах сокета, поддерживаемых Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth и всааддресстостринг](bluetooth-and-wsaaddresstostring.md)                         | используется для преобразования адреса устройства Bluetooth в строку, которая, в свою очередь, предоставляется функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) через структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) при получении сведений о службе устройства.<br/>                                           |
| [Bluetooth и всалукупсервицебегин](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth использует функцию [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запроса устройств и обнаружения служб.<br/>                                                                                                                                                                         |
| [Bluetooth и всалукупсервиценекст](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth использует функцию [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) для сопоставления запросов, указанных в предыдущем вызове функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth и всалукупсервицеенд](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth использует функцию [**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) для завершения запроса, инициированного в предыдущем вызове [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), и, возможно, расширен в последующих вызовах [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth и всакуерисет](bluetooth-and-wsaqueryset.md)                                       | Структура [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) используется в операциях, включая запрос устройства, запрос службы и настройку службы.<br/>                                                                                                                                                                |
| [Bluetooth и всасетсервице](bluetooth-and-wsasetservice.md)                                   | Bluetooth использует функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ бс) из реестра.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 


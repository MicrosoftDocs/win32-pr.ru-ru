---
description: 'Функции разрешения имен можно сгруппировать в три категории: Установка службы, клиентские запросы и вспомогательное приложение (с макросами).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Общие сведения о функциях разрешения имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809700"
---
# <a name="summary-of-name-resolution-functions"></a>Общие сведения о функциях разрешения имен

Функции разрешения имен можно сгруппировать в три категории: Установка службы, клиентские запросы и вспомогательное приложение (с макросами). В следующих разделах определяются функции в каждой категории и кратко описывается их предполагаемое использование. Также описаны основные структуры данных.

## <a name="service-installation"></a>Установка службы

-   [**всаинсталлсервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**всаремовесервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Если требуемый класс службы еще не существует, приложение использует [**всаинсталлсервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) для установки нового класса службы, указав имя класса службы, идентификатор GUID для идентификатора класса службы и ряд структур [**всансклассинфо**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Эти структуры зависят от конкретного пространства имен и предоставляют общие значения, такие как Рекомендуемые номера TCP-портов или идентификаторы NetWare SAP. Класс службы можно удалить путем вызова [**всаремовесервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) и указания идентификатора GUID, соответствующего идентификатору класса.

После существования класса службы определенные экземпляры службы можно установить или удалить с помощью [**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea). Эта функция принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входного параметра вместе с кодом операции и флагами операций. Код операции указывает, выполняется ли установка или удаление службы. Структура **всакуерисет** предоставляет все необходимые сведения о службе, включая идентификатор класса службы, имя службы (для этого экземпляра), применимый идентификатор пространства имен и сведения о протоколе, а также набор транспортных адресов, на которых служба прослушивает службу. Службы должны вызывать **всасетсервице** при инициализации для объявления их присутствия в динамических пространствах имен.

## <a name="client-query"></a>Клиентский запрос

-   [**всаенумнамеспацепровидерс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

Функция [**всаенумнамеспацепровидерс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) позволяет приложению определить, какие пространства имен доступны через средства разрешения имен Winsock. Он также позволяет приложению определить, поддерживается ли данное пространство имен несколькими поставщиками пространства имен, и определить идентификатор поставщика для любого конкретного поставщика пространства имен. С помощью идентификатора поставщика приложение может ограничить операцию запроса указанным поставщиком пространства имен.

Пространство имен Winsock — операции запроса содержат ряд вызовов: [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), за которыми следует один или несколько вызовов [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) и заканчиваются вызовом [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **Всалукупсервицебегин** принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входных данных для определения параметров запроса вместе с набором флагов для предоставления дополнительного контроля над поисковой операцией. Он возвращает маркер запроса, который используется в последующих вызовах **всалукупсервиценекст** и **всалукупсервицеенд**.

Приложение вызывает [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) для получения результатов запроса, в котором результаты передаются в буфер [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленный приложением. Приложение будет вызывать **всалукупсервиценекст** до тех пор, пока не будет возвращен код ошибки WSA \_ E, \_ \_ указывающий, что все результаты получены. После этого поиск завершается вызовом [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). Функция **всалукупсервицеенд** может также использоваться для отмены ожидающего в данный момент **всалукупсервиценекст** при вызове из другого потока.

В Windows Sockets 2 для ВСАЕНОМОРЕ (10102) и WSA \_ E ( \_ 10110) определены конфликтующие коды ошибок \_ . Код ошибки ВСАЕНОМОРЕ будет удален в следующей версии, и только WSA E больше \_ \_ не \_ останется. Однако для сокетов Windows 2 приложения должны проверять как ВСАЕНОМОРЕ, так и WSA \_ E, \_ но не \_ больше для самой широкой совместимости с поставщиками пространства имен, которые используют один из них.

## <a name="helper-functions"></a>Вспомогательные функции

-   [**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**всааддресстостринг**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**всастрингтоаддресс**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**всажетсервицеклассинфо**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

Вспомогательные функции разрешения имен включают функцию для получения имени класса службы по заданному идентификатору класса службы, пару функций, используемых для преобразования транспортного адреса между структурой [**SOCKADDR**](sockaddr-2.md) и строковым представлением ASCII, функцию для получения сведений о схеме класса службы для данного класса службы и набор макросов для сопоставления хорошо известных служб с предварительно ВЫДЕЛЕНными идентификаторами GUID.

Следующие макросы из Winsock2. h помогают в сопоставлении между известными классами служб и этими пространствами имен:

| Макрос                                                                                                            | Описание                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| СВЦИД \_ TCP (порт) свЦид \_ UDP (порт)<br/> СВЦИД \_ NetWare (тип объекта)<br/>                              | При наличии порта для TCP/IP или UDP/IP или типа объекта в случае с NetWare возвращает идентификатор GUID (номер порта в порядке размещения). |
| \_свЦид \_ TCP (GUID) — это \_ СВЦИД \_ UDP (GUID)<br/> ЯВЛЯЕТСЯ \_ свЦид \_ NetWare (GUID)<br/>                          | Возвращает **значение true** , если идентификатор GUID находится в допустимом диапазоне.                                                                |
| SET \_ TCP \_ СВЦИД (GUID, порт) Set \_ UDP \_ свЦид (GUID, порт)<br/>                                                | Инициализирует структуру GUID с эквивалентом GUID для номера порта TCP или UDP (номер порта должен быть в порядке размещения).    |
| Порт \_ из \_ \_ порта СВЦИД TCP (GUID) \_ из \_ свЦид \_ UDP (GUID)<br/> SAPI \_ из \_ свЦид \_ NetWare (GUID)<br/> | Возвращает порт или тип объекта, связанный с идентификатором GUID (номер порта в порядке размещения).                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**жетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**жетаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**жетнамеинфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Структуры данных разрешения имен](name-resolution-data-structures-2.md)
</dt> <dt>

[Модель разрешения имен](name-resolution-model-2.md)
</dt> <dt>

[Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Регистрация и разрешение имен](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**всаенумнамеспацепровидерс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**всаинсталлсервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**всаремовесервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**всансклассинфо**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 





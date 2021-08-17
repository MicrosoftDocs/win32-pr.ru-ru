---
description: Транспорт Winsock SPI аналогичен API Winsock в том, что отображаются все основные функции сокета.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Сопоставление транспорта между функциями API и SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739944"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Сопоставление транспорта между функциями API и SPI

Транспорт Winsock SPI аналогичен API Winsock в том, что отображаются все основные функции сокета. Если в API существует новая версия функции Winsock и исходная версия, в SPI будет отображаться только новая версия. Это показано в следующем списке.

-   [**Подключение**](/windows/desktop/api/Winsock2/nf-winsock2-connect) и [**всаконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) обеих карт с [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) и [**Всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) Map to [**вспакцепт**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   подключение [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) к [**вспсоккет**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Другие функции API, свернутые в расширенные версии в SPI, включают:

-   [**Отправить**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**cервера**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**полученных**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**иоктлсоккет**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Функции поддержки, такие как [**хтонл**](/windows/desktop/api/winsock/nf-winsock-htonl), [**хтонс**](/windows/desktop/api/winsock/nf-winsock-htons), [**нтохл**](/windows/desktop/api/winsock/nf-winsock-ntohl)и [**нтохс**](/windows/desktop/api/winsock/nf-winsock-ntohs) , реализуются в Ws2 \_32.dll и не передаются в поставщики услуг. То же самое справедливо и для версий WSA этих функций.

Windows Перечисление поставщиков услуг сокетов и функции блокировки, связанные с ловушками, реализованы в \_32.dll Ws2, поэтому [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [Всаисблоккинг](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [всасетблоккингхук](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)и [всаунхукблоккингхук](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) не отображаются как функции SPI.

Так как коды ошибок возвращаются вместе с функциями SPI, в SPI не требуются эквиваленты [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) и [**всасетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) .

функции обработки и ожидания объектов событий, включая [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**всаклосивент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**всасетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**всаресетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)и [**всаваитформултипливентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , сопоставляются непосредственно с собственными Windowsными службами и поэтому отсутствуют в SPI.

все функции преобразования и разрешения имен, относящиеся к протоколу TCP/IP, в Windows sockets 1,1, такие как **жетксбии**, **всаасинкжетксбии** и [**всаканцеласинкрекуест**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), [**а также в**](/windows/desktop/api/winsock/nf-winsock-gethostname) Ws2 \_32.dll с точки зрения новых средств разрешения имен. дополнительные сведения см. [в разделе совместимое разрешение имен для TCP/IP в Windows сокетах 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Функции преобразования, такие как [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) и [**inet \_ нтоа**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) , реализуются в Ws2 \_32.dll.

 

 

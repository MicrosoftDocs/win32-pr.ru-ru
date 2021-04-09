---
description: Запрос имени службы в сокетах Windows (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Запрос на обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080590"
---
# <a name="service-query"></a>Запрос на обслуживание

-   [**нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Запрос службы имен включает ряд вызовов: [**нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), за которыми следует один или несколько вызовов [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) и заканчивая вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**Нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входных данных, чтобы определить параметры запроса вместе с набором флагов, чтобы обеспечить дополнительный контроль над операцией поиска. Он возвращает маркер запроса, который используется в последующих вызовах **нсплукупсервиценекст** и **нсплукупсервицеенд**.

Клиент SPI пространства имен вызывает [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) для получения результатов запроса с результатами, предоставленными в буфере [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленном клиентом. Клиент продолжит вызывать **нсплукупсервиценекст** до тех пор, пока не будет возвращен код ошибки WSA \_ E, \_ \_ указывающий, что все результаты получены. После этого поиск завершается вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). Функция **нсплукупсервицеенд** может также использоваться для отмены ожидающего в данный момент **нсплукупсервиценекст** при вызове из другого потока.

В Windows Sockets 2 для ВСАЕНОМОРЕ (10102) и WSA \_ E ( \_ 10110) определены конфликтующие коды ошибок \_ . Код ошибки ВСАЕНОМОРЕ будет удален в следующей версии, и только WSA E больше \_ \_ не \_ останется. Поставщики пространства имен должны переключиться на использование WSA \_ E \_ без \_ кода ошибки как можно скорее, чтобы обеспечить совместимость с самым широким возможным диапазоном приложений.

 

 




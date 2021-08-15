---
description: запрос службы имен в сокетах Windows (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Запрос на обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5452c94c3768cbff387b0125fe183a3026f7ab6c64d90325341ce5f2a9366de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740423"
---
# <a name="service-query"></a>Запрос на обслуживание

-   [**нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Запрос службы имен включает ряд вызовов: [**нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), за которыми следует один или несколько вызовов [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) и заканчивая вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**Нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входных данных, чтобы определить параметры запроса вместе с набором флагов, чтобы обеспечить дополнительный контроль над операцией поиска. Он возвращает маркер запроса, который используется в последующих вызовах **нсплукупсервиценекст** и **нсплукупсервицеенд**.

Клиент SPI пространства имен вызывает [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) для получения результатов запроса с результатами, предоставленными в буфере [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленном клиентом. Клиент продолжит вызывать **нсплукупсервиценекст** до тех пор, пока не будет возвращен код ошибки WSA \_ E, \_ \_ указывающий, что все результаты получены. После этого поиск завершается вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). Функция **нсплукупсервицеенд** может также использоваться для отмены ожидающего в данный момент **нсплукупсервиценекст** при вызове из другого потока.

в соединителях Windows 2, конфликтующие коды ошибок определены для всаеноморе (10102) и WSA \_ E \_ \_ (10110). Код ошибки ВСАЕНОМОРЕ будет удален в следующей версии, и только WSA E больше \_ \_ не \_ останется. Поставщики пространства имен должны переключиться на использование WSA \_ E \_ без \_ кода ошибки как можно скорее, чтобы обеспечить совместимость с самым широким возможным диапазоном приложений.

 

 




---
title: Bluetooth и BLOB-объект
description: Bluetooth использует структуру больших двоичных объектов для передачи или получения данных, относящихся к транспорту, в структуру всакуерисет во время вызовов функций всасетсервице или всалукупсервице \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth и BLOB-объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081138"
---
# <a name="bluetooth-and-blob"></a>Bluetooth и BLOB-объект

Bluetooth использует структуру [**больших двоичных объектов**](/windows/desktop/api/nspapi/ns-nspapi-blob) для передачи или получения данных, относящихся к транспорту, в структуру [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) во время вызовов функций [**всасетсервице**](bluetooth-and-wsasetservice.md) или **всалукупсервице** \* .

для использования с Bluetooth и функцией [**всасетсервице**](bluetooth-and-wsasetservice.md) члены структуры [**большого двоичного объекта**](/windows/desktop/api/nspapi/ns-nspapi-blob) должны иметь следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы набора БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**службы БС \_ Set \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

для использования с Bluetooth и [всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)используйте следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

для использования с Bluetooth и [всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)используйте следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Дополнительные сведения см. в подразделе "Примечания" на странице справочника по структуре [**\_ \_ службы БС Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Bluetooth и всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и всасетсервице](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**ОБЪЕКТЕ**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**БС \_ запрос \_ устройства**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_служба запросов \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_Служба настройки \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**всасетсервице**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 
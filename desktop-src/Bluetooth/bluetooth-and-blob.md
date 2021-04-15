---
title: Bluetooth и большой двоичный объект
description: Bluetooth использует структуру больших двоичных объектов для передачи или получения данных, относящихся к транспорту, в структуру ВСАКУЕРИСЕТ во время вызовов функций Всасетсервице или Всалукупсервице \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth и большой двоичный объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654339"
---
# <a name="bluetooth-and-blob"></a>Bluetooth и большой двоичный объект

Bluetooth использует структуру [**больших двоичных объектов**](/windows/desktop/api/nspapi/ns-nspapi-blob) для передачи или получения данных, относящихся к транспорту, в структуру [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) во время вызовов функций [**всасетсервице**](bluetooth-and-wsasetservice.md) или **всалукупсервице** \* .

Для использования с Bluetooth и функцией [**всасетсервице**](bluetooth-and-wsasetservice.md) члены структуры [**большого двоичного объекта**](/windows/desktop/api/nspapi/ns-nspapi-blob) должны иметь следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы набора БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**службы БС \_ Set \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

Для использования с Bluetooth и [всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)используйте следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

Для использования с Bluetooth и [всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)используйте следующие параметры:

-   Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) , используемой в элементе **пблобдата** , в байтах.
-   Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Дополнительные сведения см. в подразделе "Примечания" на странице справочника по структуре [**\_ \_ службы БС Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Bluetooth и Всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и Всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и Всасетсервице](bluetooth-and-wsasetservice.md)
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

 

 
---
title: Bluetooth и всалукупсервицеенд
description: Bluetooth использует функцию всалукупсервицеенд для завершения запроса, инициированного в предыдущем вызове всалукупсервицебегин, и, возможно, расширен в последующих вызовах всалукупсервиценекст.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- всалукупсервицеенд
- Bluetooth и всалукупсервицеенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd6c893a06fbf586d07e3a2581d1d25626e161508e505dc089d7660267bae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081098"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth и всалукупсервицеенд

Bluetooth использует функцию [**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) для завершения запроса, инициированного в предыдущем вызове [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), и, возможно, расширен в последующих вызовах [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta). Вызов **всалукупсервицеенд** завершает запрос и очищает контекст.

действия по запросу устройства и обнаружению службы в Bluetooth в достаточной степени отличаются для отдельной обработки. дополнительные сведения о Bluetooth и функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запросов устройств см. в разделе [Bluetooth и всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). дополнительные сведения о Bluetooth и функции **всалукупсервицебегин** для обнаружения службы см. в разделе [Bluetooth и всалукупсервицебегин для обнаружения службы](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и всалукупсервиценекст](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**\_служба запросов \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**соединиться**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
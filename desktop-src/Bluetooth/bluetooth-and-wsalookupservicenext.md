---
title: Bluetooth и всалукупсервиценекст
description: Bluetooth использует функцию всалукупсервиценекст для сопоставления запросов, указанных в предыдущем вызове функции всалукупсервицебегин.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- всалукупсервиценекст
- Bluetooth и всалукупсервиценекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010396"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth и всалукупсервиценекст

Bluetooth использует функцию [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) для сопоставления запросов, указанных в предыдущем вызове функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). Результаты функции **всалукупсервиценекст** определяются параметрами, заданными в структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой в начальном вызове функции **всалукупсервицебегин** .

действия по запросу устройства и обнаружению службы в Bluetooth в достаточной степени отличаются для отдельной обработки. дополнительные сведения о Bluetooth и функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запросов устройств см. в разделе [Bluetooth и всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). дополнительные сведения о Bluetooth и функции **всалукупсервицебегин** для обнаружения службы см. в разделе [Bluetooth и всалукупсервицебегин для обнаружения службы](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и всалукупсервицеенд](bluetooth-and-wsalookupserviceend.md)
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
</dt> </dl>

 

 
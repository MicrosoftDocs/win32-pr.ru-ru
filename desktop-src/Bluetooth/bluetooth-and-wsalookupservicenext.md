---
title: Bluetooth и Всалукупсервиценекст
description: Bluetooth использует функцию Всалукупсервиценекст для сопоставления запросов, указанных в предыдущем вызове функции Всалукупсервицебегин.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- всалукупсервиценекст
- Bluetooth и Всалукупсервиценекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890701"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth и Всалукупсервиценекст

Bluetooth использует функцию [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) для сопоставления запросов, указанных в предыдущем вызове функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). Результаты функции **всалукупсервиценекст** определяются параметрами, заданными в структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой в начальном вызове функции **всалукупсервицебегин** .

Действия по запросу устройства и обнаружению служб в Bluetooth достаточно отличаются для отдельной обработки. Дополнительные сведения об Bluetooth и функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запросов устройств см. в разделе [Bluetooth и Всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Дополнительные сведения об Bluetooth и функции **всалукупсервицебегин** для обнаружения службы см. в разделе [Bluetooth и Всалукупсервицебегин для обнаружения службы](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth и Всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и Всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и Всалукупсервицеенд](bluetooth-and-wsalookupserviceend.md)
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

 

 
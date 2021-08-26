---
title: Обнаружение устройств и служб Bluetooth
description: чтобы упростить обнаружение Bluetooth устройств и служб, Windows сопоставляет протокол обнаружения Bluetooth Service (SDP) с интерфейсами пространств имен Windows sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, задачи, обнаружение устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004044"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Обнаружение устройств и служб Bluetooth

чтобы упростить обнаружение Bluetooth устройств и служб, Windows сопоставляет протокол обнаружения Bluetooth Service (SDP) с интерфейсами пространств имен Windows sockets. К основным функциям, используемым для этого сопоставления, относятся функции [**всасетсервице**](bluetooth-and-wsasetservice.md), [**всалукупсервицебегин**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md)и [**всалукупсервицеенд**](bluetooth-and-wsalookupserviceend.md) . Структура [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) также используется вместе с этими функциями.

поскольку некоторые понятия и параметры от SDP Bluetooth не обязательно сопоставляются непосредственно со структурой [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) , необходимо уделять внимание способам создания и использования своих членов. для многих сложных операций Bluetooth, таких как создание записей SDP, используется элемент **лпблоб** в **всакуерисет** . если необходимо учитывать такие особенности, они описаны особо, например на страницах ссылок, таких как [**Bluetooth и всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md), а также в других.

Важно понимать, что регистрация SDP отделена от управления сокетом. когда серверное приложение подготавливается к приему клиентского подключения, оно должно вызывать функцию [**всасетсервице**](bluetooth-and-wsasetservice.md) для регистрации записи SDP Bluetooth, соответствующей этой службе. это Bluetooth приложение должно снова вызвать функцию **всасетсервице** перед закрытием, чтобы отменить регистрацию записи SDP Bluetooth.

При использовании функций сопоставления, описанных на этой странице, \_ назначается пространство имен NS БС.

Дополнительные сведения об обнаружении устройств и служб см. на следующих справочных страницах:

-   [**Bluetooth и всасетсервице**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth и всалукупсервицебегин для запроса устройства**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth и всалукупсервицебегин для обнаружения служб**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth и всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth и всалукупсервицеенд**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth и BLOB-объект**](bluetooth-and-blob.md)
-   [**Bluetooth и всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md)

вы также можете скачать [пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) для получения полного примера.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Bluetooth программирование с помощью сокетов Windows](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





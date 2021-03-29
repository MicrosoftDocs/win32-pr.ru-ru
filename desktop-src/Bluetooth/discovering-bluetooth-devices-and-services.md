---
title: Обнаружение устройств и служб Bluetooth
description: Чтобы упростить обнаружение устройств и служб Bluetooth, Windows сопоставляет протокол обнаружения службы Bluetooth (SDP) с интерфейсами пространства имен Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, задачи, обнаружение устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "105654267"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Обнаружение устройств и служб Bluetooth

Чтобы упростить обнаружение устройств и служб Bluetooth, Windows сопоставляет протокол обнаружения службы Bluetooth (SDP) с интерфейсами пространства имен Windows Sockets. К основным функциям, используемым для этого сопоставления, относятся функции [**всасетсервице**](bluetooth-and-wsasetservice.md), [**всалукупсервицебегин**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md)и [**всалукупсервицеенд**](bluetooth-and-wsalookupserviceend.md) . Структура [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) также используется вместе с этими функциями.

Поскольку некоторые понятия и параметры от SDP по Bluetooth не обязательно сопоставляются непосредственно со структурой [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) , необходимо уделять внимание способам создания и использования своих членов. Для многих сложных операций Bluetooth, таких как создание записей SDP, используется элемент **лпблоб** в **всакуерисет** . Если необходимо учитывать такие особенности, они описаны особо, например на страницах ссылок, таких как [**Bluetooth и всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md), а также в других.

Важно понимать, что регистрация SDP отделена от управления сокетом. Когда серверное приложение подготавливается к приему клиентского подключения, оно должно вызвать функцию [**всасетсервице**](bluetooth-and-wsasetservice.md) , чтобы зарегистрировать запись SDP с поддержкой Bluetooth, соответствующую этой службе. Это приложение Bluetooth должно повторно вызвать функцию **всасетсервице** перед закрытием, чтобы отменить регистрацию записи SDP с Bluetooth.

При использовании функций сопоставления, описанных на этой странице, \_ назначается пространство имен NS БС.

Дополнительные сведения об обнаружении устройств и служб см. на следующих справочных страницах:

-   [**Bluetooth и Всасетсервице**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth и Всалукупсервицебегин для запроса устройства**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth и Всалукупсервицебегин для обнаружения служб**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth и Всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth и Всалукупсервицеенд**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth и большой двоичный объект**](bluetooth-and-blob.md)
-   [**Bluetooth и ВСАКУЕРИСЕТ**](bluetooth-and-wsaqueryset-for-set-service.md)

Вы также можете скачать [Пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) для получения полного примера.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Программирование Bluetooth с помощью сокетов Windows](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





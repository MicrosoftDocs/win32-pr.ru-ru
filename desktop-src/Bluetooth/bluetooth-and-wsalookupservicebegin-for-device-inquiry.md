---
title: Bluetooth и всалукупсервицебегин для запроса устройства
description: В этом разделе описывается использование функции Всалукупсервицебегин для выполнения запроса как видимых, так и несинхронизированных устройств. дополнительные сведения см. в статье обнаружение Bluetooth устройств и служб.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth и всалукупсервицебегин для запроса устройства Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4423b7c1c27124771c518409d9d1393a5f83afb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469191"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth и всалукупсервицебегин для запроса устройства

В этом разделе описывается использование функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для выполнения запроса как видимых, так и несинхронизированных устройств. дополнительные сведения см. в статье [обнаружение Bluetooth устройств и служб](discovering-bluetooth-devices-and-services.md).

Функция [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) использует структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) в своем первом параметре *лпксрестриктионс*, чтобы определить критерии поиска. Bluetooth приводятся конкретные рекомендации по использованию функции **всалукупсервицебегин** и **всакуерисет**.

В следующей таблице перечислены ограничения, которые применяются к структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой параметру *лпксрестриктионс* при запросе устройств.




| ВСАКУЕРИСЕТ, элемент | Ограничение | 
|--------------------|-------------|
| <strong>двсизе</strong> | Задайте значение <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>). | 
| <strong>лпблоб</strong> | Этот элемент содержит необязательный указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> . Если этот элемент указан, допустимые параметры запроса устройства для <strong>LUP_FLUSHCACHE</strong> следующие:<ul><li>Элемент <strong>кбсизе</strong> структуры <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> должен быть <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li><li>элемент <strong>пблобдата</strong> является указателем на структуру <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , для <strong>которой элемент в</strong> позиции является Bluetooth кодом доступа к запросу, а элемент <strong>length</strong> — это длина запроса в секундах.</li></ul> | 
| <strong>двнамеспаце</strong> | Задайте значение <strong>NS_BTH</strong>. | 
| Другие члены | Другие члены структуры <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a> игнорируются. | 




 

Флаги, перечисленные в следующей таблице, используются в параметре *двконтролфлагс* для управления результатами запроса. **Луп \_ контейнеры** и флаги **\_ флушкаче Луп** используются функцией [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) . остальные флаги используются в вызовах функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Flag               | Результат                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_контейнеры Луп    | указывает, что целью запроса является получение списка устройств Bluetooth, а не списка служб. Этот флаг должен быть установлен.                                                                                                                                                                                                                                                                                       |
| ЛУП \_ флушкаче    | Запускает запрос локальных устройств или вызывает возврат кэшированных результатов из предыдущих запросов.                                                                                                                                                                                                                                                                                                                |
| \_тип возвращаемого значения Луп \_  | возврат Bluetooth наложенного платежа (класс битов устройства) непосредственно в элемент **лпсервицеклассид** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Наложенный платеж сопоставлен с элементом **файл1** идентификатора GUID.                                                                                                                                                                                                      |
| \_Служба Луп RES \_  | возвращает сведения о локальном адресе Bluetooth. Этот флаг действует только в том случае, если также указан параметр **Луп \_ return \_ addr** .                                                                                                                                                                                                                                                                                       |
| \_имя возврата \_ Луп  | Возвращает отображаемое имя устройства в элементе **лпсзсервицеинстанценаме** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Этот флаг также должен быть указан для получения **имени** члена структуры [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при указании флага **\_ возврата BLOB- \_ объекта Луп** . |
| ЛУП \_ обратный \_ адрес  | Возвращает структуру [**\_ БС SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , содержащую 48-разрядный адрес однорангового узла в **лпксабуффере** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Другие члены структуры **\_ БС SOCKADDR** будут пустыми.                                                            |
| \_возвращаемый \_ BLOB-объект Луп  | Возвращает структуру [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при каждом последующем вызове метода [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| ЛУП \_ флушпревиаус | Пропуск следующего доступного устройства и возврат устройства, следующего за ним.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Bluetooth и всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и всалукупсервиценекст](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth и всакуерисет для запроса устройства](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**ОБЪЕКТЕ**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**БС \_ запрос \_ устройства**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 

---
title: Bluetooth и Всалукупсервицебегин для запроса устройства
description: В этом разделе описывается использование функции Всалукупсервицебегин для выполнения запроса как видимых, так и несинхронизированных устройств. Дополнительные сведения см. в разделе Обнаружение устройств и служб Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth и Всалукупсервицебегин для запроса устройства Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104134707"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth и Всалукупсервицебегин для запроса устройства

В этом разделе описывается использование функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для выполнения запроса как видимых, так и несинхронизированных устройств. Дополнительные сведения см. в разделе [обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md).

Функция [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) использует структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) в своем первом параметре *лпксрестриктионс*, чтобы определить критерии поиска. Bluetooth предоставляет конкретные рекомендации по использованию функции **всалукупсервицебегин** и **всакуерисет**.

В следующей таблице перечислены ограничения, которые применяются к структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой параметру *лпксрестриктионс* при запросе устройств.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>ВСАКУЕРИСЕТ, элемент</th>
<th>Ограничение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>двсизе</strong></td>
<td>Задайте значение <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>).</td>
</tr>
<tr class="even">
<td><strong>лпблоб</strong></td>
<td>Этот элемент содержит необязательный указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> . Если этот элемент указан, допустимые параметры запроса устройства для <strong>LUP_FLUSHCACHE</strong> следующие:
<ul>
<li>Элемент <strong>кбсизе</strong> структуры <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> должен быть <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li>
<li>Элемент <strong>пблобдата</strong> является указателем на структуру <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , для <strong>которой элемент в</strong> позиции является кодом доступа к запросу Bluetooth, а элемент <strong>length</strong> — длиной (в секундах) запроса.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>двнамеспаце</strong></td>
<td>Задайте значение <strong>NS_BTH</strong>.</td>
</tr>
<tr class="even">
<td>Другие члены</td>
<td>Другие члены структуры <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a> игнорируются.</td>
</tr>
</tbody>
</table>



 

Флаги, перечисленные в следующей таблице, используются в параметре *двконтролфлагс* для управления результатами запроса. **Луп \_ контейнеры** и флаги **\_ флушкаче Луп** используются функцией [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) . остальные флаги используются в вызовах функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Flag               | Результат                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_контейнеры Луп    | Указывает, что целью запроса является получение списка устройств Bluetooth, а не списка служб. Этот флаг должен быть установлен.                                                                                                                                                                                                                                                                                       |
| ЛУП \_ флушкаче    | Запускает запрос локальных устройств или вызывает возврат кэшированных результатов из предыдущих запросов.                                                                                                                                                                                                                                                                                                                |
| \_тип возвращаемого значения Луп \_  | Верните порт Bluetooth (класс битов устройства) непосредственно в элемент **лпсервицеклассид** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Наложенный платеж сопоставлен с элементом **файл1** идентификатора GUID.                                                                                                                                                                                                      |
| \_Служба Луп RES \_  | Возвращает сведения об локальном адресе Bluetooth. Этот флаг действует только в том случае, если также указан параметр **Луп \_ return \_ addr** .                                                                                                                                                                                                                                                                                       |
| \_имя возврата \_ Луп  | Возвращает отображаемое имя устройства в элементе **лпсзсервицеинстанценаме** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Этот флаг также должен быть указан для получения **имени** члена структуры [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при указании флага **\_ возврата BLOB- \_ объекта Луп** . |
| ЛУП \_ обратный \_ адрес  | Возвращает структуру [**\_ БС SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , содержащую 48-разрядный адрес однорангового узла в **лпксабуффере** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Другие члены структуры **\_ БС SOCKADDR** будут пустыми.                                                            |
| \_возвращаемый \_ BLOB-объект Луп  | Возвращает структуру [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при каждом последующем вызове метода [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| ЛУП \_ флушпревиаус | Пропуск следующего доступного устройства и возврат устройства, следующего за ним.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Bluetooth и Всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth и Всалукупсервиценекст](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth и ВСАКУЕРИСЕТ для запроса устройства](bluetooth-and-wsaqueryset-for-device-inquiry.md)
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

 

 
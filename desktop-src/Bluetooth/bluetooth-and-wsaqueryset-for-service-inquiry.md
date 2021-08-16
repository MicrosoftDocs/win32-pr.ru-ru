---
title: Bluetooth и всакуерисет для запроса на обслуживание
description: Использование структуры ВСАКУЕРИСЕТ с функциями Всалукупсервицебегин и Всалукупсервиценекст для получения сведений о процессе запроса службы.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth и всакуерисет для запроса на обслуживание Bluetooth
- всакуерисет Bluetooth, для запроса на обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959163"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth и всакуерисет для запроса на обслуживание

Bluetooth использует структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) с различными функциями, чтобы упростить обнаружение устройств и служб в пространстве имен Bluetooth, NS \_ бс.

Функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) и [**Всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) используют структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для получения данных о процессе запроса службы. В следующей таблице описано, как задать значения элементов в структуре **всакуерисет** для этой цели.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Член</th>
<th>Входные данные в Всалукупсервицебегин</th>
<th>Возвращенное значение из Всалукупсервиценекст</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>двсизе</strong></td>
<td>Необходимо задать значение <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>), возвращенная системой.</td>
</tr>
<tr class="even">
<td><strong>дваутпутфлагс</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td><strong>лпсзсервицеинстанценаме</strong></td>
<td>Не используется.</td>
<td>отображаемое имя службы, преобразованное как строка в кодировке UTF-8 из кодировки языка по умолчанию для атрибута Bluetooth ServiceName SDP. Возвращается, если указан LUP_RETURN_NAME.</td>
</tr>
<tr class="even">
<td><strong>лпсервицеклассид</strong></td>
<td>Обязательный. наиболее конкретный единый Bluetooth UUID для служб, для которых выполняется поиск. Например, если для этого параметра задано значение UUID протокола L2CAP, он возвращает все службы, использующие Протокол L2CAP на целевом устройстве. Если задано значение UUID определенной службы, оно вернет только экземпляры этой службы.</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td><strong>лпверсион</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="even">
<td><strong>лпсзкоммент</strong></td>
<td>Не используется.</td>
<td>описание службы, преобразованное как строка в кодировке UTF-8 из кодировки языка по умолчанию для атрибута Bluetooth ServiceDescription SDP. Возвращается, если указан <strong>LUP_RETURN_COMMENT</strong> .</td>
</tr>
<tr class="odd">
<td><strong>двнамеспаце</strong></td>
<td>Необходимо NS_BTH.</td>
<td>Возвращает NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>лпнспровидерид</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td><strong>лпсзконтекст</strong></td>
<td>Обязательный. адрес устройства Bluetooth, с помощью которого устанавливается подключение SDP и запрос к службам. Это значение должно быть строкой, которая была преобразована с помощью вызова функции <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>всааддресстостринг</strong></a> . если указан адрес локального Bluetooth устройства, выполняется поиск локальной базы данных SDP.</td>
<td>Не используется.</td>
</tr>
<tr class="even">
<td><strong>двнумберофпротоколс</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td><strong>лпафппротоколс</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="even">
<td><strong>лпсзкуеристринг</strong></td>
<td>Не используется.</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td><strong>двнумберофксаддрс</strong></td>
<td>Не используется.</td>
<td>Указывает количество элементов в массиве структур <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>лпксабуффер</strong></td>
<td>Не используется.</td>
<td>указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> , член <strong>локаладдр. лпсоккаддр</strong> которой указывает на <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> , содержащий полный подключаемый адрес удаленной службы, преобразованный из первой записи атрибута SDP Bluetooth протоколдескрипторлист. Возвращается, если указан <strong>LUP_RETURN_ADDR</strong> .</td>
</tr>
<tr class="odd">
<td><strong>лпблоб</strong></td>
<td>Необязательный элемент. Указатель на структуру <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> , содержащую дополнительные параметры для ограничения результатов поиска. Если указано, <strong>лпсервицеклассид</strong> игнорируется, а кэшированные запросы не выполняются.</td>
<td><ul>
<li>Если выполняется поиск службы: указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> , которая возвращает дескрипторы службы. (<strong>BLOB. кбсизе</strong>)/<strong>sizeof</strong>(ulong) вычисляет количество дескрипторов. <strong>BLOB. пблобдата</strong> — это массив значений ulong, представляющих дескрипторы службы.</li>
<li>Если выполняется поиск атрибута или Сервицеаттрибуте: указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> , возвращающий двоичную запись SDP. <strong>BLOB. кбсизе</strong> — размер двоичной записи SDP. <strong>BLOB. пблобдата</strong> указывает на саму запись. Двоичная запись SDP необходима во многих случаях, поскольку только ограниченное число атрибутов SDP могут быть преобразованы в структуру <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a> и преобразованы только строки UTF-8, закодированные по умолчанию. функции, помогающие при анализе двоичной записи SDP, приведены в разделе <a href="bluetooth-reference.md">справки Bluetooth</a> .</li>
<li>Возвращается, если указан LUP_RETURN_BLOB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Bluetooth и всакуерисет для Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth и всакуерисет для запроса устройства](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth и BLOB-объект](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth и всалукупсервицебегин](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth и всалукупсервиценекст
</dt> <dt>

[Bluetooth IsReference](bluetooth-reference.md)
</dt> <dt>

[**ОБЪЕКТЕ**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_служба запросов \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_сведения о ксаддр**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
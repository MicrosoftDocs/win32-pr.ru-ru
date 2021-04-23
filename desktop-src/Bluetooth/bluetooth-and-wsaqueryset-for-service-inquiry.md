---
title: Bluetooth и ВСАКУЕРИСЕТ для запроса на обслуживание
description: Использование структуры ВСАКУЕРИСЕТ с функциями Всалукупсервицебегин и Всалукупсервиценекст для получения сведений о процессе запроса службы.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth и ВСАКУЕРИСЕТ для запроса на обслуживание Bluetooth
- ВСАКУЕРИСЕТ Bluetooth, для запроса на обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795301"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="7978e-105">Bluetooth и ВСАКУЕРИСЕТ для запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="7978e-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="7978e-106">Bluetooth использует структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) с различными функциями, чтобы упростить обнаружение устройств и служб в пространстве имен Bluetooth, NS \_ БС.</span><span class="sxs-lookup"><span data-stu-id="7978e-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="7978e-107">Функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) и [**Всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) используют структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для получения данных о процессе запроса службы.</span><span class="sxs-lookup"><span data-stu-id="7978e-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="7978e-108">В следующей таблице описано, как задать значения элементов в структуре **всакуерисет** для этой цели.</span><span class="sxs-lookup"><span data-stu-id="7978e-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7978e-109">Член</span><span class="sxs-lookup"><span data-stu-id="7978e-109">Member</span></span></th>
<th><span data-ttu-id="7978e-110">Входные данные в Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="7978e-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="7978e-111">Возвращенное значение из Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="7978e-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7978e-112"><strong>двсизе</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="7978e-113">Необходимо задать значение <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="7978e-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="7978e-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>), возвращенная системой.</span><span class="sxs-lookup"><span data-stu-id="7978e-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-115"><strong>дваутпутфлагс</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="7978e-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-116">Not used.</span></span></td>
<td><span data-ttu-id="7978e-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-118"><strong>лпсзсервицеинстанценаме</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="7978e-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-119">Not used.</span></span></td>
<td><span data-ttu-id="7978e-120">Отображаемое имя службы, преобразованное как строка в кодировке UTF-8 из кодировки языка по умолчанию атрибута "Имя_службы" для службы Bluetooth ServiceName.</span><span class="sxs-lookup"><span data-stu-id="7978e-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="7978e-121">Возвращается, если указан LUP_RETURN_NAME.</span><span class="sxs-lookup"><span data-stu-id="7978e-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-122"><strong>лпсервицеклассид</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="7978e-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7978e-123">Required.</span></span> <span data-ttu-id="7978e-124">Наиболее конкретный однобайтовый идентификатор (UUID) Bluetooth для служб, для которых выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="7978e-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="7978e-125">Например, если для этого параметра задано значение UUID протокола L2CAP, он возвращает все службы, использующие Протокол L2CAP на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="7978e-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="7978e-126">Если задано значение UUID определенной службы, оно вернет только экземпляры этой службы.</span><span class="sxs-lookup"><span data-stu-id="7978e-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="7978e-127">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-128"><strong>лпверсион</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="7978e-129">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-129">Not used.</span></span></td>
<td><span data-ttu-id="7978e-130">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-131"><strong>лпсзкоммент</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="7978e-132">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-132">Not used.</span></span></td>
<td><span data-ttu-id="7978e-133">Описание службы, преобразованное как строка в кодировке UTF-8 из кодировки языка по умолчанию для атрибута "SDP" в отношении Bluetooth ServiceDescription.</span><span class="sxs-lookup"><span data-stu-id="7978e-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="7978e-134">Возвращается, если указан <strong>LUP_RETURN_COMMENT</strong> .</span><span class="sxs-lookup"><span data-stu-id="7978e-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-135"><strong>двнамеспаце</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="7978e-136">Необходимо NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="7978e-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="7978e-137">Возвращает NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="7978e-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-138"><strong>лпнспровидерид</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="7978e-139">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-139">Not used.</span></span></td>
<td><span data-ttu-id="7978e-140">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-141"><strong>лпсзконтекст</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="7978e-142">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7978e-142">Required.</span></span> <span data-ttu-id="7978e-143">Адрес устройства Bluetooth, с помощью которого устанавливается подключение SDP и запрос к службам.</span><span class="sxs-lookup"><span data-stu-id="7978e-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="7978e-144">Это значение должно быть строкой, которая была преобразована с помощью вызова функции <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>всааддресстостринг</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7978e-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="7978e-145">Если указан адрес локального устройства Bluetooth, выполняется поиск локальной базы данных SDP.</span><span class="sxs-lookup"><span data-stu-id="7978e-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="7978e-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-147"><strong>двнумберофпротоколс</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="7978e-148">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-148">Not used.</span></span></td>
<td><span data-ttu-id="7978e-149">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-150"><strong>лпафппротоколс</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="7978e-151">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-151">Not used.</span></span></td>
<td><span data-ttu-id="7978e-152">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-153"><strong>лпсзкуеристринг</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="7978e-154">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-154">Not used.</span></span></td>
<td><span data-ttu-id="7978e-155">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-156"><strong>двнумберофксаддрс</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="7978e-157">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-157">Not used.</span></span></td>
<td><span data-ttu-id="7978e-158">Указывает количество элементов в массиве структур <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7978e-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7978e-159"><strong>лпксабуффер</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="7978e-160">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7978e-160">Not used.</span></span></td>
<td><span data-ttu-id="7978e-161">Указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> , член <strong>локаладдр. лпсоккаддр</strong> которой указывает на <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> , содержащий полный подключаемый адрес удаленной службы, преобразованный из первой записи атрибута SDP протоколдескрипторлист для Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="7978e-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="7978e-162">Возвращается, если указан <strong>LUP_RETURN_ADDR</strong> .</span><span class="sxs-lookup"><span data-stu-id="7978e-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7978e-163"><strong>лпблоб</strong></span><span class="sxs-lookup"><span data-stu-id="7978e-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="7978e-164">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7978e-164">Optional.</span></span> <span data-ttu-id="7978e-165">Указатель на структуру <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> , содержащую дополнительные параметры для ограничения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7978e-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="7978e-166">Если указано, <strong>лпсервицеклассид</strong> игнорируется, а кэшированные запросы не выполняются.</span><span class="sxs-lookup"><span data-stu-id="7978e-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="7978e-167">Если выполняется поиск службы: указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> , которая возвращает дескрипторы службы.</span><span class="sxs-lookup"><span data-stu-id="7978e-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="7978e-168">(<strong>BLOB. кбсизе</strong>)/<strong>sizeof</strong>(ulong) вычисляет количество дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="7978e-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="7978e-169"><strong>BLOB. пблобдата</strong> — это массив значений ulong, представляющих дескрипторы службы.</span><span class="sxs-lookup"><span data-stu-id="7978e-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="7978e-170">Если выполняется поиск атрибута или Сервицеаттрибуте: указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> , возвращающий двоичную запись SDP.</span><span class="sxs-lookup"><span data-stu-id="7978e-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="7978e-171"><strong>BLOB. кбсизе</strong> — размер двоичной записи SDP.</span><span class="sxs-lookup"><span data-stu-id="7978e-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="7978e-172"><strong>BLOB. пблобдата</strong> указывает на саму запись.</span><span class="sxs-lookup"><span data-stu-id="7978e-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="7978e-173">Двоичная запись SDP необходима во многих случаях, поскольку только ограниченное число атрибутов SDP могут быть преобразованы в структуру <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a> и преобразованы только строки UTF-8, закодированные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7978e-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="7978e-174">Функции, помогающие при анализе двоичной записи SDP, приведены в разделе <a href="bluetooth-reference.md">справки по Bluetooth</a> .</span><span class="sxs-lookup"><span data-stu-id="7978e-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="7978e-175">Возвращается, если указан LUP_RETURN_BLOB.</span><span class="sxs-lookup"><span data-stu-id="7978e-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7978e-176">См. также</span><span class="sxs-lookup"><span data-stu-id="7978e-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7978e-177">Bluetooth и ВСАКУЕРИСЕТ для Set Service</span><span class="sxs-lookup"><span data-stu-id="7978e-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="7978e-178">Bluetooth и ВСАКУЕРИСЕТ для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="7978e-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="7978e-179">Bluetooth и большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="7978e-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="7978e-180">Bluetooth и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="7978e-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="7978e-181">Bluetooth и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="7978e-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="7978e-182">Справочник по Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7978e-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="7978e-183">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="7978e-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="7978e-184">**\_служба запросов \_ БС**</span><span class="sxs-lookup"><span data-stu-id="7978e-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="7978e-185">**\_сведения о ксаддр**</span><span class="sxs-lookup"><span data-stu-id="7978e-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="7978e-186">**SOCKADDR \_ БС**</span><span class="sxs-lookup"><span data-stu-id="7978e-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="7978e-187">**всааддресстостринг**</span><span class="sxs-lookup"><span data-stu-id="7978e-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="7978e-188">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="7978e-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="7978e-189">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="7978e-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
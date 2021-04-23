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
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="d27ef-105">Bluetooth и Всалукупсервицебегин для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="d27ef-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="d27ef-106">В этом разделе описывается использование функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для выполнения запроса как видимых, так и несинхронизированных устройств.</span><span class="sxs-lookup"><span data-stu-id="d27ef-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="d27ef-107">Дополнительные сведения см. в разделе [обнаружение устройств и служб Bluetooth](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="d27ef-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="d27ef-108">Функция [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) использует структуру [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) в своем первом параметре *лпксрестриктионс*, чтобы определить критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="d27ef-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="d27ef-109">Bluetooth предоставляет конкретные рекомендации по использованию функции **всалукупсервицебегин** и **всакуерисет**.</span><span class="sxs-lookup"><span data-stu-id="d27ef-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="d27ef-110">В следующей таблице перечислены ограничения, которые применяются к структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой параметру *лпксрестриктионс* при запросе устройств.</span><span class="sxs-lookup"><span data-stu-id="d27ef-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d27ef-111">ВСАКУЕРИСЕТ, элемент</span><span class="sxs-lookup"><span data-stu-id="d27ef-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="d27ef-112">Ограничение</span><span class="sxs-lookup"><span data-stu-id="d27ef-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d27ef-113"><strong>двсизе</strong></span><span class="sxs-lookup"><span data-stu-id="d27ef-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="d27ef-114">Задайте значение <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d27ef-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d27ef-115"><strong>лпблоб</strong></span><span class="sxs-lookup"><span data-stu-id="d27ef-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="d27ef-116">Этот элемент содержит необязательный указатель на структуру <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d27ef-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="d27ef-117">Если этот элемент указан, допустимые параметры запроса устройства для <strong>LUP_FLUSHCACHE</strong> следующие:</span><span class="sxs-lookup"><span data-stu-id="d27ef-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="d27ef-118">Элемент <strong>кбсизе</strong> структуры <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>большого двоичного объекта</strong></a> должен быть <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span><span class="sxs-lookup"><span data-stu-id="d27ef-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="d27ef-119">Элемент <strong>пблобдата</strong> является указателем на структуру <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , для <strong>которой элемент в</strong> позиции является кодом доступа к запросу Bluetooth, а элемент <strong>length</strong> — длиной (в секундах) запроса.</span><span class="sxs-lookup"><span data-stu-id="d27ef-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d27ef-120"><strong>двнамеспаце</strong></span><span class="sxs-lookup"><span data-stu-id="d27ef-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="d27ef-121">Задайте значение <strong>NS_BTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="d27ef-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d27ef-122">Другие члены</span><span class="sxs-lookup"><span data-stu-id="d27ef-122">Other members</span></span></td>
<td><span data-ttu-id="d27ef-123">Другие члены структуры <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>всакуерисет</strong></a> игнорируются.</span><span class="sxs-lookup"><span data-stu-id="d27ef-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d27ef-124">Флаги, перечисленные в следующей таблице, используются в параметре *двконтролфлагс* для управления результатами запроса.</span><span class="sxs-lookup"><span data-stu-id="d27ef-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="d27ef-125">**Луп \_ контейнеры** и флаги **\_ флушкаче Луп** используются функцией [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) . остальные флаги используются в вызовах функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="d27ef-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="d27ef-126">Flag</span><span class="sxs-lookup"><span data-stu-id="d27ef-126">Flag</span></span>               | <span data-ttu-id="d27ef-127">Результат</span><span class="sxs-lookup"><span data-stu-id="d27ef-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27ef-128">\_контейнеры Луп</span><span class="sxs-lookup"><span data-stu-id="d27ef-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="d27ef-129">Указывает, что целью запроса является получение списка устройств Bluetooth, а не списка служб.</span><span class="sxs-lookup"><span data-stu-id="d27ef-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="d27ef-130">Этот флаг должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="d27ef-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d27ef-131">ЛУП \_ флушкаче</span><span class="sxs-lookup"><span data-stu-id="d27ef-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="d27ef-132">Запускает запрос локальных устройств или вызывает возврат кэшированных результатов из предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="d27ef-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d27ef-133">\_тип возвращаемого значения Луп \_</span><span class="sxs-lookup"><span data-stu-id="d27ef-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="d27ef-134">Верните порт Bluetooth (класс битов устройства) непосредственно в элемент **лпсервицеклассид** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="d27ef-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="d27ef-135">Наложенный платеж сопоставлен с элементом **файл1** идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="d27ef-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="d27ef-136">\_Служба Луп RES \_</span><span class="sxs-lookup"><span data-stu-id="d27ef-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="d27ef-137">Возвращает сведения об локальном адресе Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d27ef-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="d27ef-138">Этот флаг действует только в том случае, если также указан параметр **Луп \_ return \_ addr** .</span><span class="sxs-lookup"><span data-stu-id="d27ef-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d27ef-139">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="d27ef-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="d27ef-140">Возвращает отображаемое имя устройства в элементе **лпсзсервицеинстанценаме** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="d27ef-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="d27ef-141">Этот флаг также должен быть указан для получения **имени** члена структуры [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при указании флага **\_ возврата BLOB- \_ объекта Луп** .</span><span class="sxs-lookup"><span data-stu-id="d27ef-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="d27ef-142">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="d27ef-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="d27ef-143">Возвращает структуру [**\_ БС SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , содержащую 48-разрядный адрес однорангового узла в **лпксабуффере** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) для каждого вызова функции [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="d27ef-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="d27ef-144">Другие члены структуры **\_ БС SOCKADDR** будут пустыми.</span><span class="sxs-lookup"><span data-stu-id="d27ef-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="d27ef-145">\_возвращаемый \_ BLOB-объект Луп</span><span class="sxs-lookup"><span data-stu-id="d27ef-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="d27ef-146">Возвращает структуру [**\_ \_ сведений об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) при каждом последующем вызове метода [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="d27ef-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d27ef-147">ЛУП \_ флушпревиаус</span><span class="sxs-lookup"><span data-stu-id="d27ef-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="d27ef-148">Пропуск следующего доступного устройства и возврат устройства, следующего за ним.</span><span class="sxs-lookup"><span data-stu-id="d27ef-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d27ef-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d27ef-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d27ef-150">Bluetooth и Всалукупсервицебегин для обнаружения служб</span><span class="sxs-lookup"><span data-stu-id="d27ef-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="d27ef-151">Bluetooth и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="d27ef-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="d27ef-152">Bluetooth и ВСАКУЕРИСЕТ для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="d27ef-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="d27ef-153">Обнаружение устройств и служб Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d27ef-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="d27ef-154">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="d27ef-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="d27ef-155">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="d27ef-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="d27ef-156">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="d27ef-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="d27ef-157">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="d27ef-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="d27ef-158">**БС \_ запрос \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="d27ef-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="d27ef-159">**SOCKADDR \_ БС**</span><span class="sxs-lookup"><span data-stu-id="d27ef-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="d27ef-160">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="d27ef-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="d27ef-161">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="d27ef-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
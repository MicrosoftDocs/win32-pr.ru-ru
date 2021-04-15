---
title: Bluetooth и большой двоичный объект
description: Bluetooth использует структуру больших двоичных объектов для передачи или получения данных, относящихся к транспорту, в структуру ВСАКУЕРИСЕТ во время вызовов функций Всасетсервице или Всалукупсервице \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth и большой двоичный объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654339"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="07a69-107">Bluetooth и большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="07a69-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="07a69-108">Bluetooth использует структуру [**больших двоичных объектов**](/windows/desktop/api/nspapi/ns-nspapi-blob) для передачи или получения данных, относящихся к транспорту, в структуру [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) во время вызовов функций [**всасетсервице**](bluetooth-and-wsasetservice.md) или **всалукупсервице** \* .</span><span class="sxs-lookup"><span data-stu-id="07a69-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="07a69-109">Для использования с Bluetooth и функцией [**всасетсервице**](bluetooth-and-wsasetservice.md) члены структуры [**большого двоичного объекта**](/windows/desktop/api/nspapi/ns-nspapi-blob) должны иметь следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="07a69-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="07a69-110">Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы набора БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) , используемой в элементе **пблобдата** , в байтах.</span><span class="sxs-lookup"><span data-stu-id="07a69-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="07a69-111">Элемент **пблобдата** должен быть указателем на структуру [**службы БС \_ Set \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="07a69-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="07a69-112">Для использования с Bluetooth и [всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="07a69-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="07a69-113">Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) , используемой в элементе **пблобдата** , в байтах.</span><span class="sxs-lookup"><span data-stu-id="07a69-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="07a69-114">Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ устройства запроса БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .</span><span class="sxs-lookup"><span data-stu-id="07a69-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="07a69-115">Для использования с Bluetooth и [всалукупсервицебегин для обнаружения служб](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="07a69-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="07a69-116">Для элемента **кбсизе** необходимо задать размер структуры [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) , используемой в элементе **пблобдата** , в байтах.</span><span class="sxs-lookup"><span data-stu-id="07a69-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="07a69-117">Элемент **пблобдата** должен быть указателем на структуру [**\_ \_ службы запросов БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .</span><span class="sxs-lookup"><span data-stu-id="07a69-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="07a69-118">Дополнительные сведения см. в подразделе "Примечания" на странице справочника по структуре [**\_ \_ службы БС Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="07a69-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a69-119">См. также</span><span class="sxs-lookup"><span data-stu-id="07a69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a69-120">Bluetooth и Всалукупсервицебегин для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="07a69-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="07a69-121">Bluetooth и Всалукупсервицебегин для обнаружения служб</span><span class="sxs-lookup"><span data-stu-id="07a69-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="07a69-122">Bluetooth и Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="07a69-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="07a69-123">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="07a69-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="07a69-124">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="07a69-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="07a69-125">**БС \_ запрос \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="07a69-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="07a69-126">**\_служба запросов \_ БС**</span><span class="sxs-lookup"><span data-stu-id="07a69-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="07a69-127">**\_Служба настройки \_ БС**</span><span class="sxs-lookup"><span data-stu-id="07a69-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="07a69-128">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="07a69-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="07a69-129">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="07a69-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="07a69-130">**всасетсервице**</span><span class="sxs-lookup"><span data-stu-id="07a69-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 
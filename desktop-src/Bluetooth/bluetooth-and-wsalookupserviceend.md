---
title: Bluetooth и Всалукупсервицеенд
description: Bluetooth использует функцию Всалукупсервицеенд для завершения запроса, инициированного в предыдущем вызове Всалукупсервицебегин, и, возможно, расширен в последующих вызовах Всалукупсервиценекст.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- всалукупсервицеенд
- Bluetooth и Всалукупсервицеенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987596"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="364d7-106">Bluetooth и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="364d7-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="364d7-107">Bluetooth использует функцию [**всалукупсервицеенд**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) для завершения запроса, инициированного в предыдущем вызове [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), и, возможно, расширен в последующих вызовах [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="364d7-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="364d7-108">Вызов **всалукупсервицеенд** завершает запрос и очищает контекст.</span><span class="sxs-lookup"><span data-stu-id="364d7-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="364d7-109">Действия по запросу устройства и обнаружению служб в Bluetooth достаточно отличаются для отдельной обработки.</span><span class="sxs-lookup"><span data-stu-id="364d7-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="364d7-110">Дополнительные сведения об Bluetooth и функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запросов устройств см. в разделе [Bluetooth и Всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="364d7-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="364d7-111">Дополнительные сведения об Bluetooth и функции **всалукупсервицебегин** для обнаружения службы см. в разделе [Bluetooth и Всалукупсервицебегин для обнаружения службы](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="364d7-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="364d7-112">См. также</span><span class="sxs-lookup"><span data-stu-id="364d7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="364d7-113">Обнаружение устройств и служб Bluetooth</span><span class="sxs-lookup"><span data-stu-id="364d7-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="364d7-114">Bluetooth и Всалукупсервицебегин для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="364d7-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="364d7-115">Bluetooth и Всалукупсервицебегин для обнаружения служб</span><span class="sxs-lookup"><span data-stu-id="364d7-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="364d7-116">Bluetooth и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="364d7-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="364d7-117">**\_служба запросов \_ БС**</span><span class="sxs-lookup"><span data-stu-id="364d7-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="364d7-118">**соединиться**</span><span class="sxs-lookup"><span data-stu-id="364d7-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="364d7-119">**SOCKADDR \_ БС**</span><span class="sxs-lookup"><span data-stu-id="364d7-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="364d7-120">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="364d7-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="364d7-121">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="364d7-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="364d7-122">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="364d7-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="364d7-123">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="364d7-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="364d7-124">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="364d7-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
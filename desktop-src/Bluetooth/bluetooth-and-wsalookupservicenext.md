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
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="28686-106">Bluetooth и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="28686-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="28686-107">Bluetooth использует функцию [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) для сопоставления запросов, указанных в предыдущем вызове функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span><span class="sxs-lookup"><span data-stu-id="28686-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="28686-108">Результаты функции **всалукупсервиценекст** определяются параметрами, заданными в структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , передаваемой в начальном вызове функции **всалукупсервицебегин** .</span><span class="sxs-lookup"><span data-stu-id="28686-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="28686-109">Действия по запросу устройства и обнаружению служб в Bluetooth достаточно отличаются для отдельной обработки.</span><span class="sxs-lookup"><span data-stu-id="28686-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="28686-110">Дополнительные сведения об Bluetooth и функции [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) для запросов устройств см. в разделе [Bluetooth и Всалукупсервицебегин для запроса устройства](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="28686-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="28686-111">Дополнительные сведения об Bluetooth и функции **всалукупсервицебегин** для обнаружения службы см. в разделе [Bluetooth и Всалукупсервицебегин для обнаружения службы](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="28686-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28686-112">См. также</span><span class="sxs-lookup"><span data-stu-id="28686-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28686-113">Обнаружение устройств и служб Bluetooth</span><span class="sxs-lookup"><span data-stu-id="28686-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="28686-114">Bluetooth и Всалукупсервицебегин для запроса устройства</span><span class="sxs-lookup"><span data-stu-id="28686-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="28686-115">Bluetooth и Всалукупсервицебегин для обнаружения служб</span><span class="sxs-lookup"><span data-stu-id="28686-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="28686-116">Bluetooth и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="28686-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="28686-117">**\_служба запросов \_ БС**</span><span class="sxs-lookup"><span data-stu-id="28686-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="28686-118">**соединиться**</span><span class="sxs-lookup"><span data-stu-id="28686-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="28686-119">**SOCKADDR \_ БС**</span><span class="sxs-lookup"><span data-stu-id="28686-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="28686-120">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="28686-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="28686-121">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="28686-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="28686-122">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="28686-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="28686-123">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="28686-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 
---
description: Вспомогательная служба IP предоставляет возможности управления сетевыми адаптерами. Между интерфейсами и адаптерами на данном компьютере имеется однозначное соответствие. Интерфейс — это абстракция на уровне IP, тогда как адаптер является абстракцией на уровне канала передачи.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Управление сетевыми адаптерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541215"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="337d5-105">Управление сетевыми адаптерами</span><span class="sxs-lookup"><span data-stu-id="337d5-105">Managing Network Adapters</span></span>

<span data-ttu-id="337d5-106">Вспомогательная служба IP предоставляет возможности управления сетевыми адаптерами.</span><span class="sxs-lookup"><span data-stu-id="337d5-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="337d5-107">Между интерфейсами и адаптерами на данном компьютере имеется однозначное соответствие.</span><span class="sxs-lookup"><span data-stu-id="337d5-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="337d5-108">Интерфейс — это абстракция на уровне IP, тогда как адаптер является абстракцией на уровне канала передачи.</span><span class="sxs-lookup"><span data-stu-id="337d5-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="337d5-109">Используйте функции, описанные в следующих абзацах, чтобы получить сведения о сетевых адаптерах на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="337d5-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="337d5-110">Функция [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) возвращает массив структур [**\_ \_ сведений об IP-адаптере**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , по одному для каждого адаптера на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="337d5-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="337d5-111">Функция [**жетперадаптеринфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) Возвращает дополнительные сведения о конкретном адаптере.</span><span class="sxs-lookup"><span data-stu-id="337d5-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="337d5-112">Функция **жетперадаптеринфо** требует, чтобы вызывающий объект указал индекс адаптера.</span><span class="sxs-lookup"><span data-stu-id="337d5-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="337d5-113">Чтобы получить индекс адаптера из имени адаптера, используйте функцию [**жетадаптериндекс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .</span><span class="sxs-lookup"><span data-stu-id="337d5-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="337d5-114">Некоторые приложения используют адаптеры, которые получают датаграммы, но не могут их передавать.</span><span class="sxs-lookup"><span data-stu-id="337d5-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="337d5-115">Чтобы получить сведения об этих адаптерах, используйте функцию [**жетунидиректионаладаптеринфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .</span><span class="sxs-lookup"><span data-stu-id="337d5-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="337d5-116">Функция [**жетадаптерсаддрессес**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) позволяет получать IP-адреса, связанные с определенным адаптером.</span><span class="sxs-lookup"><span data-stu-id="337d5-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="337d5-117">Эта функция поддерживает адресацию IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="337d5-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="337d5-118">Примеры кода, включающие [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , см. [в разделе Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="337d5-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 




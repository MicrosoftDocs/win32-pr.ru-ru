---
description: В этом разделе описывается многоадресное программирование на основе финального состояния с помощью IOCTL вместо параметров сокета. Общие сведения о том, как окончательное многоадресное программирование на основе изменений отличается от многоадресного программирования на основе изменения, см. в разделе многоадресное программирование.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Многоадресное программирование на основе конечного состояния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701530"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="4caa1-104">Многоадресное программирование на основе конечного состояния</span><span class="sxs-lookup"><span data-stu-id="4caa1-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="4caa1-105">В этом разделе описывается многоадресное программирование на основе финального состояния с помощью IOCTL вместо параметров сокета.</span><span class="sxs-lookup"><span data-stu-id="4caa1-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="4caa1-106">Общие сведения о том, как окончательное многоадресное программирование на основе изменений отличается от многоадресного программирования на основе изменения, см. в разделе [многоадресное](multicast-programming.md)программирование.</span><span class="sxs-lookup"><span data-stu-id="4caa1-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="4caa1-107">В следующей таблице описаны IOCTL сокетов Windows, используемые для многоадресного программирования в Windows.</span><span class="sxs-lookup"><span data-stu-id="4caa1-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="4caa1-108">ЗАПРОС</span><span class="sxs-lookup"><span data-stu-id="4caa1-108">IOCTL</span></span>                       | <span data-ttu-id="4caa1-109">Тип аргумента</span><span class="sxs-lookup"><span data-stu-id="4caa1-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="4caa1-110">сиоксмсфилтер</span><span class="sxs-lookup"><span data-stu-id="4caa1-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="4caa1-111">[**Группа \_ Структура фильтра**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter)</span><span class="sxs-lookup"><span data-stu-id="4caa1-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="4caa1-112">сиокгмсфилтер</span><span class="sxs-lookup"><span data-stu-id="4caa1-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="4caa1-113">[**Группа \_ Структура фильтра**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter)</span><span class="sxs-lookup"><span data-stu-id="4caa1-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="4caa1-114">\_Получение \_ многоадресного \_ фильтра SIO</span><span class="sxs-lookup"><span data-stu-id="4caa1-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="4caa1-115">Структура [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="4caa1-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="4caa1-116">\_ \_ Многоадресный \_ Фильтр набора SIO</span><span class="sxs-lookup"><span data-stu-id="4caa1-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="4caa1-117">Структура [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="4caa1-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="4caa1-118">Обратите внимание, что ioctl **сиоксмсфилтер** и **Сиокгмсфилтер** доступны в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="4caa1-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="4caa1-119">Использование этих IOCTL для многоадресного программирования имеет выигрыш в производительности при работе с большими списками источников.</span><span class="sxs-lookup"><span data-stu-id="4caa1-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="4caa1-120">Дополнительные сведения о параметрах и параметрах, связанных с использованием SIO \_ Получение \_ фильтра многоадресной рассылки \_ или \_ набора SIO Настройка \_ многоадресного \_ фильтра, см. на странице справочника по [**\_ фильтрам групп**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) .</span><span class="sxs-lookup"><span data-stu-id="4caa1-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="4caa1-121">Дополнительные сведения о параметрах и параметрах, связанных с использованием SIO \_ получить \_ Фильтр многоадресной рассылки \_ или \_ набор SIO \_ \_ , см. на странице справочника по [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .</span><span class="sxs-lookup"><span data-stu-id="4caa1-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 




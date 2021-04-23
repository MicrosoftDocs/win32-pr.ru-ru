---
title: Типы сведений IPX для блоков сведений маршрутизатора
description: Следующие типы сведений перечислены в Ипксртдеф. h. Используйте эти типы данных с блоками данных маршрутизатора при выполнении транспорта IPX.
ms.assetid: 6cbc8415-f5ba-4f84-a23f-dd4f4a54d118
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4494da951c04433da2cf9b1da20db7ea5f3119
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070369"
---
# <a name="ipx-information-types-for-router-information-blocks"></a><span data-ttu-id="9529a-104">Типы сведений IPX для блоков сведений маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="9529a-104">IPX Information Types for Router Information Blocks</span></span>

<span data-ttu-id="9529a-105">Следующие типы сведений перечислены в Ипксртдеф. h.</span><span class="sxs-lookup"><span data-stu-id="9529a-105">The following information types are listed in Ipxrtdef.h.</span></span> <span data-ttu-id="9529a-106">Используйте эти типы данных с блоками данных маршрутизатора при выполнении транспорта IPX.</span><span class="sxs-lookup"><span data-stu-id="9529a-106">Use these information types with the router information block functions when running the IPX transport.</span></span>



| <span data-ttu-id="9529a-107">Тип информации</span><span class="sxs-lookup"><span data-stu-id="9529a-107">Information type</span></span>                              | <span data-ttu-id="9529a-108">Структура информации</span><span class="sxs-lookup"><span data-stu-id="9529a-108">Information structure</span></span>                                          |
|-----------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9529a-109">\_ \_ тип сведений о АДАПТЕРе IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-109">IPX\_ADAPTER\_INFO\_TYPE</span></span>                      | <span data-ttu-id="9529a-110">\_сведения о адаптере IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-110">IPX\_ADAPTER\_INFO</span></span>                                             |
| <span data-ttu-id="9529a-111">\_глобальный \_ тип сведений \_ IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-111">IPX\_GLOBAL\_INFO\_TYPE</span></span>                       | <span data-ttu-id="9529a-112">\_глобальные \_ сведения IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-112">IPX\_GLOBAL\_INFO</span></span>                                              |
| <span data-ttu-id="9529a-113">\_ \_ тип сведений об ИНТЕРФЕЙСе IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-113">IPX\_INTERFACE\_INFO\_TYPE</span></span>                    | [<span data-ttu-id="9529a-114">**\_данные IPX if \_**</span><span class="sxs-lookup"><span data-stu-id="9529a-114">**IPX\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipx_if_info)                           |
| <span data-ttu-id="9529a-115">\_ \_ \_ \_ \_ тип глобальной информации фильтра \_ трафика IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-115">IPX\_IN\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span>  | <span data-ttu-id="9529a-116">\_ \_ \_ глобальные \_ сведения фильтрации трафика IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-116">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="9529a-117">\_ \_ \_ \_ глобальный \_ \_ тип фильтрации трафика IPX out</span><span class="sxs-lookup"><span data-stu-id="9529a-117">IPX\_OUT\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span> | <span data-ttu-id="9529a-118">\_ \_ \_ глобальные \_ сведения фильтрации трафика IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-118">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="9529a-119">\_ \_ \_ \_ тип сведений о фильтре трафика IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-119">IPX\_IN\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>          | <span data-ttu-id="9529a-120">\_ \_ сведения о фильтре трафика IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-120">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="9529a-121">\_ \_ \_ \_ тип сведений фильтрации трафика IPX out \_</span><span class="sxs-lookup"><span data-stu-id="9529a-121">IPX\_OUT\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>         | <span data-ttu-id="9529a-122">\_ \_ сведения о фильтре трафика IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-122">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="9529a-123">\_тип статических \_ NetBIOS \_ - \_ имен \_ IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-123">IPX\_STATIC\_NETBIOS\_NAME\_INFO\_TYPE</span></span>        | <span data-ttu-id="9529a-124">\_ \_ сведения о статическом NetBIOS- \_ имени \_ IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-124">IPX\_STATIC\_NETBIOS\_NAME\_INFO</span></span>                               |
| <span data-ttu-id="9529a-125">\_ \_ \_ тип сведений статического маршрута \_ IPX</span><span class="sxs-lookup"><span data-stu-id="9529a-125">IPX\_STATIC\_ROUTE\_INFO\_TYPE</span></span>                | <span data-ttu-id="9529a-126">\_ \_ сведения о статическом МАРШРУТе IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-126">IPX\_STATIC\_ROUTE\_INFO</span></span>                                       |
| <span data-ttu-id="9529a-127">\_ \_ \_ тип сведений о статической службе IPX \_</span><span class="sxs-lookup"><span data-stu-id="9529a-127">IPX\_STATIC\_SERVICE\_INFO\_TYPE</span></span>              | <span data-ttu-id="9529a-128">[**\_ \_ сведения о СТАТИЧЕСКОЙ службе IPX \_**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9529a-128">[**IPX\_STATIC\_SERVICE\_INFO**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span></span> |
| <span data-ttu-id="9529a-129">\_ \_ тип сведений об ИНТЕРФЕЙСе ипксван \_</span><span class="sxs-lookup"><span data-stu-id="9529a-129">IPXWAN\_INTERFACE\_INFO\_TYPE</span></span>                 | [<span data-ttu-id="9529a-130">**ИПКСВАН, \_ Если \_ info**</span><span class="sxs-lookup"><span data-stu-id="9529a-130">**IPXWAN\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipxwan_if_info)                     |



 

 

 
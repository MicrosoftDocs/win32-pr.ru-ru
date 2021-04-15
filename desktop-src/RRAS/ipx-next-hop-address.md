---
title: Структура IPX_NEXT_HOP_ADDRESS (RTM. h)
description: '\_ \_ Структура адреса следующего прыжка IPX \_ содержит адрес маршрутизатора следующего прыжка для IPX-маршрута.'
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- RAS структуры IPX_NEXT_HOP_ADDRESS
- RAS — указатель структуры PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488949"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="bef77-105">\_ \_ Структура адреса следующего ПРЫЖКа IPX \_</span><span class="sxs-lookup"><span data-stu-id="bef77-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="bef77-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bef77-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bef77-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="bef77-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bef77-108">Структура **\_ \_ \_ адреса следующего прыжка IPX** содержит адрес маршрутизатора следующего прыжка для IPX-маршрута.</span><span class="sxs-lookup"><span data-stu-id="bef77-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef77-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bef77-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="bef77-110">Члены</span><span class="sxs-lookup"><span data-stu-id="bef77-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="bef77-111">**НХА \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="bef77-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="bef77-112">Указывает MAC-адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="bef77-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bef77-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bef77-113">Requirements</span></span>



| <span data-ttu-id="bef77-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bef77-114">Requirement</span></span> | <span data-ttu-id="bef77-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bef77-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bef77-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bef77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bef77-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bef77-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="bef77-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bef77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bef77-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bef77-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bef77-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bef77-120">End of server support</span></span><br/>    | <span data-ttu-id="bef77-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bef77-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="bef77-122">Header</span><span class="sxs-lookup"><span data-stu-id="bef77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef77-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bef77-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef77-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bef77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef77-125">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="bef77-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bef77-126">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="bef77-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="bef77-127">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="bef77-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 






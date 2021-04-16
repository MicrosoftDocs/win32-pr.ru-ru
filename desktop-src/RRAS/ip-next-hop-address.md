---
title: Структура IP_NEXT_HOP_ADDRESS (RTM. h)
description: Структура IP \_ - \_ адреса следующего прыжка \_ содержит адрес маршрутизатора следующего ПРЫЖКА для IP-маршрута.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS структуры IP_NEXT_HOP_ADDRESS
- RAS структуры PIP_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650387"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="930c6-105">\_ \_ Структура адреса следующего ПРЫЖКа IP \_</span><span class="sxs-lookup"><span data-stu-id="930c6-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="930c6-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="930c6-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="930c6-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="930c6-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="930c6-108">Структура **IP \_ - \_ \_ адреса следующего прыжка** содержит адрес маршрутизатора следующего прыжка для IP-маршрута.</span><span class="sxs-lookup"><span data-stu-id="930c6-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="930c6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="930c6-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="930c6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="930c6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="930c6-111">**N \_ нетнумбер**</span><span class="sxs-lookup"><span data-stu-id="930c6-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="930c6-112">Указывает адрес IP-сети, выраженный в виде IP-адреса в порядке байтов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="930c6-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="930c6-113">**N \_ Маска сети**</span><span class="sxs-lookup"><span data-stu-id="930c6-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="930c6-114">Указывает маску сети.</span><span class="sxs-lookup"><span data-stu-id="930c6-114">Specifies the network mask.</span></span> <span data-ttu-id="930c6-115">Примените эту маску к IP-адресу, чтобы извлечь сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="930c6-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="930c6-116">Маска сети находится в порядке байтов на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="930c6-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="930c6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="930c6-117">Remarks</span></span>

<span data-ttu-id="930c6-118">Структура **IP \_ - \_ \_ адреса следующего прыжка** является определением структуры [**IP- \_ сети**](ip-network.md) .</span><span class="sxs-lookup"><span data-stu-id="930c6-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="930c6-119">Typedef находится в RTM. h.</span><span class="sxs-lookup"><span data-stu-id="930c6-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="930c6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="930c6-120">Requirements</span></span>



| <span data-ttu-id="930c6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="930c6-121">Requirement</span></span> | <span data-ttu-id="930c6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="930c6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="930c6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="930c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="930c6-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="930c6-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="930c6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="930c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="930c6-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="930c6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="930c6-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="930c6-127">End of server support</span></span><br/>    | <span data-ttu-id="930c6-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="930c6-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="930c6-129">Header</span><span class="sxs-lookup"><span data-stu-id="930c6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="930c6-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="930c6-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930c6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="930c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930c6-132">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="930c6-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="930c6-133">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="930c6-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="930c6-134">**IP- \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="930c6-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="930c6-135">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="930c6-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 






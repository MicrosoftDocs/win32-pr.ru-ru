---
title: Структура IPX_NETWORK (RTM. h)
description: '\_Структура сети IPX описывает сетевой адрес IPX.'
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- RAS структуры IPX_NETWORK
- RAS — указатель структуры PIPX_NETWORK
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988165"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="5fccd-105">\_Структура сети IPX</span><span class="sxs-lookup"><span data-stu-id="5fccd-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="5fccd-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5fccd-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5fccd-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="5fccd-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5fccd-108">Структура **\_ сети IPX** описывает сетевой адрес IPX.</span><span class="sxs-lookup"><span data-stu-id="5fccd-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fccd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fccd-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="5fccd-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5fccd-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5fccd-111">**N \_ нетнумбер**</span><span class="sxs-lookup"><span data-stu-id="5fccd-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5fccd-112">Содержит номер сети IPX в порядке байтов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5fccd-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fccd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5fccd-113">Requirements</span></span>



| <span data-ttu-id="5fccd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5fccd-114">Requirement</span></span> | <span data-ttu-id="5fccd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5fccd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fccd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fccd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fccd-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5fccd-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="5fccd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fccd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fccd-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5fccd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5fccd-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5fccd-120">End of server support</span></span><br/>    | <span data-ttu-id="5fccd-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fccd-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5fccd-122">Header</span><span class="sxs-lookup"><span data-stu-id="5fccd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fccd-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fccd-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fccd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fccd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fccd-125">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="5fccd-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5fccd-126">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="5fccd-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="5fccd-127">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="5fccd-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 






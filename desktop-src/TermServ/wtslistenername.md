---
title: ВТСЛИСТЕНЕРНАМЕ (WtsApi32. h)
description: Представляет имя службы удаленных рабочих столов прослушивателей на сервере узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- втслистенернамев
- втслистенернамеа
- втслистенернаме
- пвтслистенернаме
- втслистенернаме
- пвтслистенернаме
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415828"
---
# <a name="wtslistenername"></a><span data-ttu-id="b63da-109">втслистенернаме</span><span class="sxs-lookup"><span data-stu-id="b63da-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="b63da-110">Представляет имя службы удаленных рабочих столов прослушивателей на сервере узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="b63da-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="b63da-111">**втслистенернамев**</span><span class="sxs-lookup"><span data-stu-id="b63da-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-112">Имя в Юникоде прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="b63da-113">**втслистенернамеа**</span><span class="sxs-lookup"><span data-stu-id="b63da-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-114">Указатель на имя в формате ANSI прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="b63da-115">**втслистенернаме**</span><span class="sxs-lookup"><span data-stu-id="b63da-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-116">Имя прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="b63da-117">**пвтслистенернаме**</span><span class="sxs-lookup"><span data-stu-id="b63da-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-118">Указатель на имя прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="b63da-119">**втслистенернаме**</span><span class="sxs-lookup"><span data-stu-id="b63da-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-120">Имя прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="b63da-121">**пвтслистенернаме**</span><span class="sxs-lookup"><span data-stu-id="b63da-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="b63da-122">Указатель на имя прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b63da-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b63da-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b63da-123">Requirements</span></span>



| <span data-ttu-id="b63da-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b63da-124">Requirement</span></span> | <span data-ttu-id="b63da-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b63da-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b63da-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b63da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b63da-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b63da-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="b63da-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b63da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b63da-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b63da-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="b63da-130">Header</span><span class="sxs-lookup"><span data-stu-id="b63da-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b63da-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="b63da-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 






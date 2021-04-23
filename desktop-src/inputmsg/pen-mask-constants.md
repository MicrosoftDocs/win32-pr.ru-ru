---
title: Маска пера
description: Значения, которые могут отображаться в поле Пенмаск структуры POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136487"
---
# <a name="pen-mask"></a><span data-ttu-id="14ae0-103">Маска пера</span><span class="sxs-lookup"><span data-stu-id="14ae0-103">Pen Mask</span></span>

<span data-ttu-id="14ae0-104">Значения, которые могут отображаться в поле **пенмаск** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="14ae0-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="14ae0-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="14ae0-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ae0-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14ae0-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="14ae0-107">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14ae0-107">Default.</span></span> <span data-ttu-id="14ae0-108">Все необязательные поля являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="14ae0-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14ae0-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="14ae0-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ae0-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ae0-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="14ae0-111">неправильное **давление** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="14ae0-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14ae0-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="14ae0-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ae0-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="14ae0-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="14ae0-114">Допускается **вращение** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="14ae0-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14ae0-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="14ae0-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ae0-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="14ae0-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="14ae0-117">**тилткс** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) является допустимой.</span><span class="sxs-lookup"><span data-stu-id="14ae0-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14ae0-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="14ae0-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ae0-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="14ae0-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="14ae0-120">**наклон** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="14ae0-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14ae0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="14ae0-121">Requirements</span></span>



| <span data-ttu-id="14ae0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="14ae0-122">Requirement</span></span> | <span data-ttu-id="14ae0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="14ae0-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14ae0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14ae0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14ae0-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="14ae0-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="14ae0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14ae0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14ae0-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="14ae0-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14ae0-128">Header</span><span class="sxs-lookup"><span data-stu-id="14ae0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14ae0-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="14ae0-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ae0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14ae0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ae0-131">Константы</span><span class="sxs-lookup"><span data-stu-id="14ae0-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="14ae0-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="14ae0-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 






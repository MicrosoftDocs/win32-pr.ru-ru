---
title: Маска касания
description: Значения, которые могут отображаться в поле Таучмаск структуры POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492645"
---
# <a name="touch-mask"></a><span data-ttu-id="a6514-103">Маска касания</span><span class="sxs-lookup"><span data-stu-id="a6514-103">Touch Mask</span></span>

<span data-ttu-id="a6514-104">Значения, которые могут отображаться в поле **таучмаск** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a6514-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="a6514-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="a6514-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6514-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6514-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="a6514-107">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6514-107">Default.</span></span> <span data-ttu-id="a6514-108">Все необязательные поля являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="a6514-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6514-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="a6514-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6514-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a6514-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="a6514-111">**ркконтакт** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) является допустимой.</span><span class="sxs-lookup"><span data-stu-id="a6514-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6514-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="a6514-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6514-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a6514-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="a6514-114">допустима **ориентация** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a6514-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6514-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="a6514-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6514-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a6514-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="a6514-117">неправильное **давление** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a6514-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6514-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a6514-118">Requirements</span></span>



| <span data-ttu-id="a6514-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a6514-119">Requirement</span></span> | <span data-ttu-id="a6514-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a6514-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6514-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6514-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6514-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a6514-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6514-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6514-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6514-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a6514-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6514-125">Header</span><span class="sxs-lookup"><span data-stu-id="a6514-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6514-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6514-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6514-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6514-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6514-128">Константы</span><span class="sxs-lookup"><span data-stu-id="a6514-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="a6514-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="a6514-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 






---
title: Флаги пера
description: Значения, которые могут отображаться в поле Пенфлагс структуры POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491841"
---
# <a name="pen-flags"></a><span data-ttu-id="bdf83-103">Флаги пера</span><span class="sxs-lookup"><span data-stu-id="bdf83-103">Pen Flags</span></span>

<span data-ttu-id="bdf83-104">Значения, которые могут отображаться в поле **пенфлагс** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bdf83-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="bdf83-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="bdf83-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdf83-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf83-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="bdf83-107">Флаг пера отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bdf83-107">There is no pen flag.</span></span> <span data-ttu-id="bdf83-108">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bdf83-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bdf83-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="bdf83-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdf83-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bdf83-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="bdf83-111">Нажата кнопка с назначением пера.</span><span class="sxs-lookup"><span data-stu-id="bdf83-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bdf83-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="bdf83-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdf83-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bdf83-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="bdf83-114">Перо будет инвертировано.</span><span class="sxs-lookup"><span data-stu-id="bdf83-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bdf83-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="bdf83-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdf83-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bdf83-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="bdf83-117">Нажата кнопка Ластик.</span><span class="sxs-lookup"><span data-stu-id="bdf83-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdf83-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bdf83-118">Requirements</span></span>



| <span data-ttu-id="bdf83-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bdf83-119">Requirement</span></span> | <span data-ttu-id="bdf83-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf83-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf83-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdf83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf83-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bdf83-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bdf83-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdf83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf83-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bdf83-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bdf83-125">Header</span><span class="sxs-lookup"><span data-stu-id="bdf83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf83-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf83-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf83-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdf83-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf83-128">Константы</span><span class="sxs-lookup"><span data-stu-id="bdf83-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="bdf83-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="bdf83-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 






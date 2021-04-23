---
title: Сообщение TBM_SETTIPSIDE (Коммктрл. h)
description: Размещает элемент управления ToolTip, используемый элементом управления TrackBar. Элементы управления TrackBar, использующие всплывающие подсказки в \_ стиле подсказок TBS.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Элементы управления Windows для TBM_SETTIPSIDE сообщений
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415137"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="d0b0d-105">\_Сообщение ТБМ сеттипсиде</span><span class="sxs-lookup"><span data-stu-id="d0b0d-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="d0b0d-106">Размещает элемент управления ToolTip, используемый элементом управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="d0b0d-107">Элементы управления TrackBar, использующие всплывающие подсказки в стиле [**\_ подсказок TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b0d-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0b0d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0b0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0b0d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b0d-110">Значение, представляющее расположение, в котором отображается элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="d0b0d-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-111">This value can be one of the following:</span></span>



| <span data-ttu-id="d0b0d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b0d-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d0b0d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b0d-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="d0b0d-114"><dt>**ТБТС \_ сверху**</dt></span><span class="sxs-lookup"><span data-stu-id="d0b0d-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="d0b0d-115">Элемент управления ToolTip будет расположен над TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="d0b0d-116">Этот флаг предназначен для использования с горизонтальными TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="d0b0d-117"><dt>**ТБТС \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="d0b0d-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="d0b0d-118">Элемент управления ToolTip будет расположен слева от TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="d0b0d-119">Этот флаг предназначен для использования с вертикальными TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="d0b0d-120"><dt>**ТБТС \_ снизу**</dt></span><span class="sxs-lookup"><span data-stu-id="d0b0d-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="d0b0d-121">Элемент управления ToolTip будет расположен под TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="d0b0d-122">Этот флаг предназначен для использования с горизонтальными TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="d0b0d-123"><dt>**ТБТС \_ вправо**</dt></span><span class="sxs-lookup"><span data-stu-id="d0b0d-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="d0b0d-124">Элемент управления ToolTip будет расположен справа от TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="d0b0d-125">Этот флаг предназначен для использования с вертикальными TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d0b0d-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0b0d-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d0b0d-127">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b0d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0b0d-128">Return value</span></span>

<span data-ttu-id="d0b0d-129">Возвращает значение, представляющее предыдущее расположение элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="d0b0d-130">Возвращаемое значение равно одному из возможных значений параметра *wParam*.</span><span class="sxs-lookup"><span data-stu-id="d0b0d-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b0d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d0b0d-131">Requirements</span></span>



| <span data-ttu-id="d0b0d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d0b0d-132">Requirement</span></span> | <span data-ttu-id="d0b0d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b0d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b0d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0b0d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b0d-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0b0d-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0b0d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0b0d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b0d-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0b0d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0b0d-138">Header</span><span class="sxs-lookup"><span data-stu-id="d0b0d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b0d-139"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b0d-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






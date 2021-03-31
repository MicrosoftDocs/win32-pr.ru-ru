---
title: Сообщение TBM_SETRANGE (Коммктрл. h)
description: Задает диапазон минимальных и максимальных логических позиций ползунка в TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Элементы управления Windows для TBM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071375"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="553d4-104">\_Сообщение SETRANGE ТБМ</span><span class="sxs-lookup"><span data-stu-id="553d4-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="553d4-105">Задает диапазон минимальных и максимальных логических позиций ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="553d4-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="553d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="553d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="553d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="553d4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="553d4-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="553d4-108">Redraw flag.</span></span> <span data-ttu-id="553d4-109">Если этот параметр имеет **значение true**, то после установки диапазона значение TrackBar перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="553d4-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="553d4-110">Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.</span><span class="sxs-lookup"><span data-stu-id="553d4-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="553d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="553d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="553d4-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает минимальное положение ползунка, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает максимальное положение.</span><span class="sxs-lookup"><span data-stu-id="553d4-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="553d4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="553d4-113">Return value</span></span>

<span data-ttu-id="553d4-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="553d4-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="553d4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="553d4-115">Remarks</span></span>

<span data-ttu-id="553d4-116">Если текущая позиция ползунка находится за пределами нового диапазона, сообщение **ТБМ \_ SETRANGE** задает для ползунка значение нового максимального или минимального значения.</span><span class="sxs-lookup"><span data-stu-id="553d4-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="553d4-117">Так как это сообщение принимает 2 16-разрядные целочисленные значения без знака, максимальный диапазон, который может указывать это сообщение, — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="553d4-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="553d4-118">Чтобы указать большие значения диапазона, используйте сообщения [**ТБМ \_ Сетранжемин**](tbm-setrangemin.md) и [**ТБМ \_ сетранжемакс**](tbm-setrangemax.md) .</span><span class="sxs-lookup"><span data-stu-id="553d4-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="553d4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="553d4-119">Requirements</span></span>



| <span data-ttu-id="553d4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="553d4-120">Requirement</span></span> | <span data-ttu-id="553d4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="553d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="553d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="553d4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="553d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="553d4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="553d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="553d4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="553d4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="553d4-126">Header</span><span class="sxs-lookup"><span data-stu-id="553d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="553d4-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="553d4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553d4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="553d4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="553d4-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="553d4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="553d4-130">**ТБМ \_ сетранжемакс**</span><span class="sxs-lookup"><span data-stu-id="553d4-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="553d4-131">**ТБМ \_ сетранжемин**</span><span class="sxs-lookup"><span data-stu-id="553d4-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 


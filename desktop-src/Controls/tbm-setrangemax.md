---
title: Сообщение TBM_SETRANGEMAX (Коммктрл. h)
description: Задает максимальное логическое положение ползунка в TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Элементы управления Windows для TBM_SETRANGEMAX сообщений
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489027"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="762dd-104">\_Сообщение ТБМ сетранжемакс</span><span class="sxs-lookup"><span data-stu-id="762dd-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="762dd-105">Задает максимальное логическое положение ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="762dd-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="762dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="762dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="762dd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="762dd-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="762dd-108">Redraw flag.</span></span> <span data-ttu-id="762dd-109">Если этот параметр имеет **значение true**, то после установки диапазона значение TrackBar перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="762dd-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="762dd-110">Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.</span><span class="sxs-lookup"><span data-stu-id="762dd-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="762dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="762dd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="762dd-112">Максимальное положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="762dd-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762dd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="762dd-113">Return value</span></span>

<span data-ttu-id="762dd-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="762dd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="762dd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="762dd-115">Remarks</span></span>

<span data-ttu-id="762dd-116">Если текущая позиция ползунка больше, чем максимальный размер, сообщение **ТБМ \_ сетранжемакс** устанавливает для ползунка новое максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="762dd-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="762dd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="762dd-117">Requirements</span></span>



| <span data-ttu-id="762dd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="762dd-118">Requirement</span></span> | <span data-ttu-id="762dd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="762dd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="762dd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="762dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="762dd-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="762dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="762dd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="762dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="762dd-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="762dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="762dd-124">Header</span><span class="sxs-lookup"><span data-stu-id="762dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="762dd-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="762dd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762dd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="762dd-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="762dd-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="762dd-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="762dd-128">**ТБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="762dd-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="762dd-129">**ТБМ \_ сетранжемин**</span><span class="sxs-lookup"><span data-stu-id="762dd-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 






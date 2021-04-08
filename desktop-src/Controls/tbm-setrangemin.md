---
title: Сообщение TBM_SETRANGEMIN (Коммктрл. h)
description: Задает минимальное логическое положение ползунка в TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Элементы управления Windows для TBM_SETRANGEMIN сообщений
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988188"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="54345-104">\_Сообщение ТБМ сетранжемин</span><span class="sxs-lookup"><span data-stu-id="54345-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="54345-105">Задает минимальное логическое положение ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="54345-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="54345-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54345-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54345-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54345-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54345-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="54345-108">Redraw flag.</span></span> <span data-ttu-id="54345-109">Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона.</span><span class="sxs-lookup"><span data-stu-id="54345-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="54345-110">Если этот параметр имеет **значение false**, сообщение задает диапазон, но не перерисовывает линейку.</span><span class="sxs-lookup"><span data-stu-id="54345-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="54345-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54345-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54345-112">Минимальная позиция ползунка.</span><span class="sxs-lookup"><span data-stu-id="54345-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54345-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54345-113">Return value</span></span>

<span data-ttu-id="54345-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="54345-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54345-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54345-115">Remarks</span></span>

<span data-ttu-id="54345-116">Если текущая позиция ползунка меньше, чем новая минимальная, сообщение **ТБМ \_ сетранжемин** устанавливает положение ползунка в новое минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="54345-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54345-117">Требования</span><span class="sxs-lookup"><span data-stu-id="54345-117">Requirements</span></span>



| <span data-ttu-id="54345-118">Требование</span><span class="sxs-lookup"><span data-stu-id="54345-118">Requirement</span></span> | <span data-ttu-id="54345-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54345-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54345-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54345-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54345-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54345-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54345-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54345-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54345-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54345-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54345-124">Header</span><span class="sxs-lookup"><span data-stu-id="54345-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54345-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="54345-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54345-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54345-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="54345-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="54345-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54345-128">**ТБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="54345-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="54345-129">**ТБМ \_ сетранжемакс**</span><span class="sxs-lookup"><span data-stu-id="54345-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 






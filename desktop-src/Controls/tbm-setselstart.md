---
title: Сообщение TBM_SETSELSTART (Коммктрл. h)
description: Задает начальную логическую точку текущего диапазона выбора в TrackBar. Это сообщение пропускается, если значение TrackBar не имеет \_ стиля TBS енаблеселранже.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Элементы управления Windows для TBM_SETSELSTART сообщений
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071103"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="774a9-105">\_Сообщение ТБМ сетселстарт</span><span class="sxs-lookup"><span data-stu-id="774a9-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="774a9-106">Задает начальную логическую точку текущего диапазона выбора в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="774a9-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="774a9-107">Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="774a9-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="774a9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="774a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774a9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="774a9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="774a9-110">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="774a9-110">Redraw flag.</span></span> <span data-ttu-id="774a9-111">Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="774a9-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="774a9-112">Если этот параметр имеет **значение false**, то сообщение задает диапазон выбора, но не перерисовывает линейку.</span><span class="sxs-lookup"><span data-stu-id="774a9-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="774a9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="774a9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="774a9-114">Начальное расположение диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="774a9-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774a9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="774a9-115">Return value</span></span>

<span data-ttu-id="774a9-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="774a9-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="774a9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="774a9-117">Requirements</span></span>



| <span data-ttu-id="774a9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="774a9-118">Requirement</span></span> | <span data-ttu-id="774a9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="774a9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="774a9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="774a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="774a9-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="774a9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="774a9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="774a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="774a9-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="774a9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="774a9-124">Header</span><span class="sxs-lookup"><span data-stu-id="774a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="774a9-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="774a9-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774a9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="774a9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="774a9-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="774a9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="774a9-128">**ТБМ \_ жетселенд**</span><span class="sxs-lookup"><span data-stu-id="774a9-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="774a9-129">**ТБМ \_ жетселстарт**</span><span class="sxs-lookup"><span data-stu-id="774a9-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="774a9-130">**ТБМ \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="774a9-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="774a9-131">**ТБМ \_ сетселенд**</span><span class="sxs-lookup"><span data-stu-id="774a9-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 






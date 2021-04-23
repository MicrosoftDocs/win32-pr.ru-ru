---
title: Сообщение TBM_SETSEL (Коммктрл. h)
description: Задает начальную и конечную позиции для доступного диапазона выбора в TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Элементы управления Windows для TBM_SETSEL сообщений
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801078"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="7e213-104">\_Сообщение ТБМ сетсел</span><span class="sxs-lookup"><span data-stu-id="7e213-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="7e213-105">Задает начальную и конечную позиции для доступного диапазона выбора в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="7e213-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e213-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e213-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e213-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e213-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="7e213-108">Redraw flag.</span></span> <span data-ttu-id="7e213-109">Если этот параметр имеет **значение true**, сообщение перерисовывается после установки диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="7e213-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="7e213-110">Если этот параметр имеет **значение false**, то сообщение задает диапазон выбора, но не перерисовывает линейку.</span><span class="sxs-lookup"><span data-stu-id="7e213-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="7e213-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e213-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e213-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает начальную логическую точку для диапазона выбора, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает конечную логическую точку.</span><span class="sxs-lookup"><span data-stu-id="7e213-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e213-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e213-113">Return value</span></span>

<span data-ttu-id="7e213-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7e213-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e213-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e213-115">Remarks</span></span>

<span data-ttu-id="7e213-116">Это сообщение пропускается, если значение TrackBar не имеет стиля [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7e213-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="7e213-117">**ТБМ \_ СЕТСЕЛ** позволяет ограничить указатель только частью диапазона, доступного индикатору выполнения.</span><span class="sxs-lookup"><span data-stu-id="7e213-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e213-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7e213-118">Requirements</span></span>



| <span data-ttu-id="7e213-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7e213-119">Requirement</span></span> | <span data-ttu-id="7e213-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7e213-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e213-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e213-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e213-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e213-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e213-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e213-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e213-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e213-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e213-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e213-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e213-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e213-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e213-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e213-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e213-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7e213-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e213-129">**ТБМ \_ жетселенд**</span><span class="sxs-lookup"><span data-stu-id="7e213-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="7e213-130">**ТБМ \_ жетселстарт**</span><span class="sxs-lookup"><span data-stu-id="7e213-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="7e213-131">**ТБМ \_ сетселенд**</span><span class="sxs-lookup"><span data-stu-id="7e213-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="7e213-132">**ТБМ \_ сетселстарт**</span><span class="sxs-lookup"><span data-stu-id="7e213-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 


---
title: Сообщение MCM_GETMONTHRANGE (Коммктрл. h)
description: Извлекает сведения о дате (с использованием структур SYSTEMTIME), представляющие верхние и малые границы отображаемого элемента управления календаря. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетмонсранже.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Элементы управления Windows для MCM_GETMONTHRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654728"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="194df-105">\_Сообщение MCM жетмонсранже</span><span class="sxs-lookup"><span data-stu-id="194df-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="194df-106">Извлекает сведения о дате (с использованием структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ), представляющие верхние и малые границы отображаемого элемента управления календаря.</span><span class="sxs-lookup"><span data-stu-id="194df-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="194df-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетмонсранже**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .</span><span class="sxs-lookup"><span data-stu-id="194df-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="194df-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="194df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="194df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="194df-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="194df-110">Значение, указывающее область возвращаемых пределов диапазона.</span><span class="sxs-lookup"><span data-stu-id="194df-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="194df-111">Это значение должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="194df-111">This value must be one of the following:</span></span>



| <span data-ttu-id="194df-112">Значение</span><span class="sxs-lookup"><span data-stu-id="194df-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="194df-113">Значение</span><span class="sxs-lookup"><span data-stu-id="194df-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="194df-114"><dt>**ГМР \_ дайстате**</dt></span><span class="sxs-lookup"><span data-stu-id="194df-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="194df-115">Включить предыдущие и конечные месяцы видимого диапазона, которые отображаются только частично.</span><span class="sxs-lookup"><span data-stu-id="194df-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="194df-116"><dt>**\_видимый ГМР**</dt></span><span class="sxs-lookup"><span data-stu-id="194df-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="194df-117">Включить только те месяцы, которые отображаются полностью.</span><span class="sxs-lookup"><span data-stu-id="194df-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="194df-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="194df-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="194df-119">Указатель на массив структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами, который получит нижний и верхний пределы области, заданной параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="194df-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="194df-120">Нижний и верхний пределы помещаются в *лпргсистимеаррай* \[ 0 \] и *лпргсистимеаррай* \[ 1 \] соответственно.</span><span class="sxs-lookup"><span data-stu-id="194df-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="194df-121">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="194df-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="194df-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="194df-122">Return value</span></span>

<span data-ttu-id="194df-123">Возвращает значение типа INT, представляющее диапазон в месяцах, охватываемый двумя ограничениями, возвращаемыми при *lParam*.</span><span class="sxs-lookup"><span data-stu-id="194df-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="194df-124">Требования</span><span class="sxs-lookup"><span data-stu-id="194df-124">Requirements</span></span>



| <span data-ttu-id="194df-125">Требование</span><span class="sxs-lookup"><span data-stu-id="194df-125">Requirement</span></span> | <span data-ttu-id="194df-126">Значение</span><span class="sxs-lookup"><span data-stu-id="194df-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="194df-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="194df-127">Minimum supported client</span></span><br/> | <span data-ttu-id="194df-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="194df-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="194df-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="194df-129">Minimum supported server</span></span><br/> | <span data-ttu-id="194df-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="194df-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="194df-131">Header</span><span class="sxs-lookup"><span data-stu-id="194df-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="194df-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="194df-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194df-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="194df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194df-134">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="194df-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 


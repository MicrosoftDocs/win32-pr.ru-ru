---
title: Сообщение DTM_SETMCCOLOR (Коммктрл. h)
description: Задает цвет для заданной части месячного календаря в элементе управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Сетмонскалколор DateTime.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Элементы управления Windows для DTM_SETMCCOLOR сообщений
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803071"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="cfbe9-105">\_Сообщение DTM сетмкколор</span><span class="sxs-lookup"><span data-stu-id="cfbe9-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="cfbe9-106">Задает цвет для заданной части месячного календаря в элементе управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="cfbe9-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="cfbe9-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетмонскалколор DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="cfbe9-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfbe9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfbe9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbe9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfbe9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbe9-110">Значение типа **int** , указывающее, какой цвет календаря месяца нужно задать.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="cfbe9-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-111">This value can be one of the following:</span></span>



| <span data-ttu-id="cfbe9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cfbe9-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="cfbe9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cfbe9-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="cfbe9-114"><dt>**\_фон MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="cfbe9-115">Задает цвет фона, отображаемый в интервале между месяцами.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="cfbe9-116"><dt>**MCSC \_ монсбк**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="cfbe9-117">Задайте цвет фона, отображаемый в пределах месяца.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="cfbe9-118"><dt>**MCSC \_ текст**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="cfbe9-119">Задайте цвет, используемый для показа текста в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="cfbe9-120"><dt>**MCSC \_ титлебк**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="cfbe9-121">Задайте цвет фона, отображаемый в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="cfbe9-122"><dt>**MCSC \_ титлетекст**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="cfbe9-123">Задайте цвет, используемый для показа текста в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="cfbe9-124"><dt>**MCSC \_ траилингтекст**</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="cfbe9-125">Задайте цвет, используемый для вывода текста заголовка и дня конца.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="cfbe9-126">Дни заголовков и конечных дней — это дни предыдущего и следующего месяцев, которые отображаются в календаре текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cfbe9-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfbe9-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbe9-128">Значение **COLORREF** , представляющее цвет, который будет задан для указанной области в месячном календаре.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbe9-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfbe9-129">Return value</span></span>

<span data-ttu-id="cfbe9-130">Возвращает значение **COLORREF** , представляющее предыдущий цвет для указанной части элемента управления "календарь месяца" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="cfbe9-131">В противном случае сообщение возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbe9-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfbe9-132">Remarks</span></span>

<span data-ttu-id="cfbe9-133">Если стили оформления включены, это сообщение не действует, кроме случаев, когда *wParam* имеет MCSC \_ Background.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbe9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cfbe9-134">Requirements</span></span>



| <span data-ttu-id="cfbe9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cfbe9-135">Requirement</span></span> | <span data-ttu-id="cfbe9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cfbe9-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbe9-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfbe9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbe9-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfbe9-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfbe9-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfbe9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbe9-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfbe9-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfbe9-141">Header</span><span class="sxs-lookup"><span data-stu-id="cfbe9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbe9-142"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe9-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






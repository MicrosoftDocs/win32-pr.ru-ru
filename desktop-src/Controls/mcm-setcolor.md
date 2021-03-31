---
title: Сообщение MCM_SETCOLOR (Коммктрл. h)
description: Задает цвет для данной части элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетколор.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Элементы управления Windows для MCM_SETCOLOR сообщений
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137438"
---
# <a name="mcm_setcolor-message"></a><span data-ttu-id="cad92-105">\_Сообщение MCM сетколор</span><span class="sxs-lookup"><span data-stu-id="cad92-105">MCM\_SETCOLOR message</span></span>

<span data-ttu-id="cad92-106">Задает цвет для данной части элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="cad92-106">Sets the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="cad92-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетколор**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .</span><span class="sxs-lookup"><span data-stu-id="cad92-107">You can send this message explicitly or by using the [**MonthCal\_SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cad92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cad92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cad92-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cad92-110">Значение типа **int** , указывающее, какой цвет календаря месяца нужно задать.</span><span class="sxs-lookup"><span data-stu-id="cad92-110">Value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="cad92-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="cad92-111">This value can be one of the following:</span></span>



| <span data-ttu-id="cad92-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cad92-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="cad92-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cad92-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="cad92-114"><dt>**\_фон MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="cad92-115">Задает цвет фона, отображаемый в интервале между месяцами.</span><span class="sxs-lookup"><span data-stu-id="cad92-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="cad92-116"><dt>**MCSC \_ монсбк**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="cad92-117">Задайте цвет фона, отображаемый в пределах месяца.</span><span class="sxs-lookup"><span data-stu-id="cad92-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="cad92-118"><dt>**MCSC \_ текст**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="cad92-119">Задайте цвет, используемый для показа текста в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="cad92-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="cad92-120"><dt>**MCSC \_ титлебк**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="cad92-121">Задайте цвет фона, отображаемый в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="cad92-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="cad92-122"><dt>**MCSC \_ титлетекст**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="cad92-123">Задайте цвет, используемый для показа текста в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="cad92-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="cad92-124"><dt>**MCSC \_ траилингтекст**</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="cad92-125">Задайте цвет, используемый для вывода текста заголовка и дня конца.</span><span class="sxs-lookup"><span data-stu-id="cad92-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="cad92-126">Дни заголовков и конечных дней — это дни предыдущего и следующего месяцев, которые отображаются в календаре текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="cad92-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cad92-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cad92-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cad92-128">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее цвет, который будет задан для указанной области в месячном календаре.</span><span class="sxs-lookup"><span data-stu-id="cad92-128">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad92-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cad92-129">Return value</span></span>

<span data-ttu-id="cad92-130">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет для указанной части элемента управления "календарь месяца" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="cad92-130">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="cad92-131">В противном случае возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="cad92-131">Otherwise, the return is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad92-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cad92-132">Remarks</span></span>

<span data-ttu-id="cad92-133">Если визуальные стили активны, это сообщение не действует, кроме случаев, когда *wParam* имеет значение MCSC \_ Background.</span><span class="sxs-lookup"><span data-stu-id="cad92-133">If visual styles are active, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad92-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cad92-134">Requirements</span></span>



| <span data-ttu-id="cad92-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cad92-135">Requirement</span></span> | <span data-ttu-id="cad92-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cad92-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cad92-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cad92-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cad92-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cad92-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cad92-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cad92-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cad92-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cad92-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cad92-141">Header</span><span class="sxs-lookup"><span data-stu-id="cad92-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cad92-142"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cad92-142"><dt>Commctrl.h</dt></span></span> </dl> |



 


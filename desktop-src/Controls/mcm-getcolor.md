---
title: Сообщение MCM_GETCOLOR (Коммктрл. h)
description: Возвращает цвет для заданной части элемента управления "Календарь на месяц". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- Элементы управления Windows для MCM_GETCOLOR сообщений
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137083"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="4e375-105">\_Сообщение MCM Color</span><span class="sxs-lookup"><span data-stu-id="4e375-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="4e375-106">Возвращает цвет для заданной части элемента управления "Календарь на месяц".</span><span class="sxs-lookup"><span data-stu-id="4e375-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="4e375-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .</span><span class="sxs-lookup"><span data-stu-id="4e375-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e375-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e375-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e375-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e375-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e375-110">Значение типа **int** , указывающее цвет месячного календаря для получения.</span><span class="sxs-lookup"><span data-stu-id="4e375-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="4e375-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="4e375-111">This value can be one of the following:</span></span>



| <span data-ttu-id="4e375-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4e375-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="4e375-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4e375-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="4e375-114"><dt>**\_фон MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="4e375-115">Получение цвета фона, отображаемого в интервале между месяцами.</span><span class="sxs-lookup"><span data-stu-id="4e375-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="4e375-116"><dt>**MCSC \_ монсбк**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="4e375-117">Получение цвета фона, отображаемого в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="4e375-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="4e375-118"><dt>**MCSC \_ текст**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="4e375-119">Получение цвета, используемого для показа текста в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="4e375-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="4e375-120"><dt>**MCSC \_ титлебк**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="4e375-121">Получение цвета фона, отображаемого в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="4e375-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="4e375-122"><dt>**MCSC \_ титлетекст**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="4e375-123">Получение цвета, используемого для показа текста в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="4e375-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="4e375-124"><dt>**MCSC \_ траилингтекст**</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="4e375-125">Получение цвета, используемого для вывода текста заголовка и конца дня.</span><span class="sxs-lookup"><span data-stu-id="4e375-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="4e375-126">Дни заголовков и конечных дней — это дни предыдущего и следующего месяцев, которые отображаются в календаре текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="4e375-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e375-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e375-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e375-128">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4e375-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e375-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e375-129">Return value</span></span>

<span data-ttu-id="4e375-130">Возвращает значение **COLORREF** , представляющее параметр цвета для указанной части элемента управления "месячный календарь" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="4e375-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="4e375-131">В противном случае это сообщение возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="4e375-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e375-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4e375-132">Requirements</span></span>



| <span data-ttu-id="4e375-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4e375-133">Requirement</span></span> | <span data-ttu-id="4e375-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4e375-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e375-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e375-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4e375-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e375-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e375-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e375-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4e375-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e375-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e375-139">Header</span><span class="sxs-lookup"><span data-stu-id="4e375-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e375-140"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e375-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






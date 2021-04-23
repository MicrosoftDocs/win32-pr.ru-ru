---
title: Сообщение DTM_GETMCCOLOR (Коммктрл. h)
description: Возвращает цвет для заданной части месячного календаря в элементе управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Жетмонскалколор DateTime.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- Элементы управления Windows для DTM_GETMCCOLOR сообщений
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493347"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="c0b59-105">\_Сообщение DTM жетмкколор</span><span class="sxs-lookup"><span data-stu-id="c0b59-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="c0b59-106">Возвращает цвет для заданной части месячного календаря в элементе управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="c0b59-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="c0b59-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетмонскалколор DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="c0b59-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0b59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0b59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0b59-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b59-110">Значение типа **int** , указывающее, какой цвет календаря месяца получить.</span><span class="sxs-lookup"><span data-stu-id="c0b59-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="c0b59-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="c0b59-111">This value can be one of the following:</span></span>



| <span data-ttu-id="c0b59-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="c0b59-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="c0b59-114"><dt>**\_фон MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="c0b59-115">Получение цвета фона, отображаемого в интервале между месяцами.</span><span class="sxs-lookup"><span data-stu-id="c0b59-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="c0b59-116"><dt>**MCSC \_ монсбк**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="c0b59-117">Получение цвета фона, отображаемого в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="c0b59-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="c0b59-118"><dt>**MCSC \_ текст**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="c0b59-119">Получение цвета, используемого для показа текста в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="c0b59-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="c0b59-120"><dt>**MCSC \_ титлебк**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="c0b59-121">Получение цвета фона, отображаемого в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="c0b59-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="c0b59-122"><dt>**MCSC \_ титлетекст**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="c0b59-123">Получение цвета, используемого для показа текста в заголовке календаря.</span><span class="sxs-lookup"><span data-stu-id="c0b59-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="c0b59-124"><dt>**MCSC \_ траилингтекст**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="c0b59-125">Получение цвета, используемого для вывода текста заголовка и конца дня.</span><span class="sxs-lookup"><span data-stu-id="c0b59-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="c0b59-126">Дни заголовков и конечных дней — это дни предыдущего и следующего месяцев, которые отображаются в календаре текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="c0b59-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0b59-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0b59-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0b59-128">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c0b59-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b59-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-129">Return value</span></span>

<span data-ttu-id="c0b59-130">Возвращает значение **COLORREF** , представляющее параметр цвета для указанной части элемента управления "месячный календарь" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="c0b59-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="c0b59-131">В случае неудачи сообщение возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="c0b59-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b59-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c0b59-132">Requirements</span></span>



| <span data-ttu-id="c0b59-133">Требование</span><span class="sxs-lookup"><span data-stu-id="c0b59-133">Requirement</span></span> | <span data-ttu-id="c0b59-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b59-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0b59-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b59-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0b59-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0b59-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0b59-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b59-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0b59-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0b59-139">Header</span><span class="sxs-lookup"><span data-stu-id="c0b59-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b59-140"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






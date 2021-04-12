---
title: Ошибки mciSendString
description: Ошибки mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Возвращаемые значения МЦИЕРР, ошибки mciSendString
- Ссылка на мультимедиа, ошибки mciSendString
- Справочник по мультимедиа, mciSendString ошибкам
- Интерфейс управления мультимедиа (MCI), ошибки mciSendString
- MCI (интерфейс управления мультимедиа), ошибки mciSendString
- Справочник по MCI, mciSendString Errors
- Справочник MCI, ошибки mciSendString
- Интерфейс управления мультимедиа (MCI), ошибки
- MCI (интерфейс управления мультимедийными файлами), ошибки
- Справочник по MCI, ошибкам
- Ссылка MCI, ошибки
- ошибки mciSendString
- Функция mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890568"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="9f940-116">Ошибки mciSendString</span><span class="sxs-lookup"><span data-stu-id="9f940-116">mciSendString Errors</span></span>

<span data-ttu-id="9f940-117">Функция [**mciSendString**](/previous-versions//dd757161(v=vs.85)) возвращает следующие ошибки, но не [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="9f940-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="9f940-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f940-118">Value</span></span>                             | <span data-ttu-id="9f940-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9f940-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="9f940-120">МЦИЕРР \_ неверная \_ константа</span><span class="sxs-lookup"><span data-stu-id="9f940-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="9f940-121">Значение, указанное для параметра, неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9f940-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="9f940-122">МЦИЕРР \_ неверное \_ целое число</span><span class="sxs-lookup"><span data-stu-id="9f940-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="9f940-123">Целое число в команде недопустимо или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9f940-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="9f940-124">МЦИЕРР \_ повторяющихся \_ флагов</span><span class="sxs-lookup"><span data-stu-id="9f940-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="9f940-125">Флаг или значение указано дважды.</span><span class="sxs-lookup"><span data-stu-id="9f940-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="9f940-126">МЦИЕРР \_ отсутствует \_ \_ Строка команды</span><span class="sxs-lookup"><span data-stu-id="9f940-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="9f940-127">Команда не указана.</span><span class="sxs-lookup"><span data-stu-id="9f940-127">No command was specified.</span></span>                         |
| <span data-ttu-id="9f940-128">МЦИЕРР \_ отсутствует \_ \_ имя устройства</span><span class="sxs-lookup"><span data-stu-id="9f940-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="9f940-129">Не указано имя устройства.</span><span class="sxs-lookup"><span data-stu-id="9f940-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="9f940-130">МЦИЕРР \_ отсутствует \_ строковый \_ аргумент</span><span class="sxs-lookup"><span data-stu-id="9f940-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="9f940-131">Строковое значение отсутствовало в команде.</span><span class="sxs-lookup"><span data-stu-id="9f940-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="9f940-132">для МЦИЕРР \_ New \_ требуется \_ псевдоним</span><span class="sxs-lookup"><span data-stu-id="9f940-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="9f940-133">Псевдоним должен использоваться с именем устройства "New".</span><span class="sxs-lookup"><span data-stu-id="9f940-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="9f940-134">МЦИЕРР \_ без \_ закрывающей \_ кавычки</span><span class="sxs-lookup"><span data-stu-id="9f940-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="9f940-135">Отсутствует закрывающая кавычка.</span><span class="sxs-lookup"><span data-stu-id="9f940-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="9f940-136">МЦИЕРР \_ уведомлять \_ при \_ автоматическом \_ открытии</span><span class="sxs-lookup"><span data-stu-id="9f940-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="9f940-137">Флаг "notify" недопустим при автоматическом открытии.</span><span class="sxs-lookup"><span data-stu-id="9f940-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="9f940-138">\_ \_ переполнение параметра мЦиерр</span><span class="sxs-lookup"><span data-stu-id="9f940-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="9f940-139">Выходная строка недостаточно длинна.</span><span class="sxs-lookup"><span data-stu-id="9f940-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="9f940-140">\_внутреннее средство синтаксического анализа мЦиерр \_</span><span class="sxs-lookup"><span data-stu-id="9f940-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="9f940-141">Произошла внутренняя ошибка средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9f940-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="9f940-142">МЦИЕРР \_ НЕраспознанное \_ ключевое слово</span><span class="sxs-lookup"><span data-stu-id="9f940-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="9f940-143">Указан неизвестный параметр команды.</span><span class="sxs-lookup"><span data-stu-id="9f940-143">An unknown command parameter was specified.</span></span>       |



 

 

 
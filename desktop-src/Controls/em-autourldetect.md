---
title: Сообщение EM_AUTOURLDETECT (RichEdit. h)
description: Включает или отключает автоматическое обнаружение гиперссылок с помощью расширенного элемента управления "поле ввода".
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Элементы управления Windows для EM_AUTOURLDETECT сообщений
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988917"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="e1681-104">\_Сообщение АУТАУРЛДЕТЕКТ EM</span><span class="sxs-lookup"><span data-stu-id="e1681-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="e1681-105">Включает или отключает автоматическое обнаружение гиперссылок с помощью расширенного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e1681-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1681-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1681-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1681-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1681-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1681-108">Укажите 0, чтобы отключить автоматическое обнаружение ссылок, или одно из следующих значений, чтобы включить различные типы обнаружения.</span><span class="sxs-lookup"><span data-stu-id="e1681-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="e1681-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e1681-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="e1681-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e1681-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="e1681-111"><dt>**АУРЛ \_ дисаблемикседлгк**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="e1681-112">**Windows 8**. Отключите распознавание доменных имен, содержащих метки, с символами, принадлежащими более чем одному из следующих сценариев: латиница, греческий и кириллица.</span><span class="sxs-lookup"><span data-stu-id="e1681-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="e1681-113"><dt>**АУРЛ \_ енабледривелеттерс**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="e1681-114">**Windows 8**: распознают имена файлов с ведущим описанием диска, например c: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="e1681-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="e1681-115"><dt>**АУРЛ \_ енаблиа**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="e1681-116">Это значение является устаревшим; Вместо этого используйте **аурл \_ енаблиаурлс** .</span><span class="sxs-lookup"><span data-stu-id="e1681-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="e1681-117"><dt>**АУРЛ \_ енаблиаурлс**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="e1681-118">Распознают URL-адреса, содержащие символы восточноазиатских языков.</span><span class="sxs-lookup"><span data-stu-id="e1681-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="e1681-119"><dt>**АУРЛ \_ енаблимаиладдр**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="e1681-120">**Windows 8**: распознают адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e1681-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="e1681-121"><dt>**АУРЛ \_ енаблетелно**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="e1681-122">**Windows 8**: распознавание телефонных номеров.</span><span class="sxs-lookup"><span data-stu-id="e1681-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="e1681-123"><dt>**АУРЛ \_ енаблеурл**</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="e1681-124">**Windows 8**: распознают URL-адреса, содержащие путь.</span><span class="sxs-lookup"><span data-stu-id="e1681-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="e1681-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1681-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1681-126">Этот параметр определяет схемы URL-адресов, распознаваемые, если активна **аурл \_ енаблеурл** .</span><span class="sxs-lookup"><span data-stu-id="e1681-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="e1681-127">Если параметр *lParam* имеет значение null, используется список имен схем по умолчанию (см. раздел Примечания).</span><span class="sxs-lookup"><span data-stu-id="e1681-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="e1681-128">Кроме того, *lParam* может указывать на строку, завершающуюся нулем, которая состоит из до 50 имен схем, заканчивающихся двоеточием, которые заменяют список имен схем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1681-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="e1681-129">Например, строка может иметь значение "News: http: FTP: Telnet:".</span><span class="sxs-lookup"><span data-stu-id="e1681-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="e1681-130">Синтаксис имени схемы определяется в универсальном [коде ресурсов (URI): документе общего синтаксиса]( https://www.ietf.org/rfc/rfc2396.txt) на веб-сайте Internet Engineering Task Force (IETF).</span><span class="sxs-lookup"><span data-stu-id="e1681-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="e1681-131">В частности, имя схемы может содержать до 13 символов (включая двоеточие), должно начинаться с буквенно-десятичного символа ASCII, а за ним можно использовать комбинацию ASCII алфабетикс, цифр и трех знаков препинания: ".", "+" и "-".</span><span class="sxs-lookup"><span data-stu-id="e1681-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="e1681-132">Строковый тип может быть либо **char \** _, _*либо \* WCHAR\*_; элемент управления Rich Edit автоматически определяет тип.</span><span class="sxs-lookup"><span data-stu-id="e1681-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1681-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1681-133">Return value</span></span>

<span data-ttu-id="e1681-134">Если сообщение прошло удачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e1681-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="e1681-135">Если сообщение не выполняется, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="e1681-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="e1681-136">Например, сообщение может завершиться ошибкой из-за нехватки памяти, недопустимого параметра обнаружения или неправильной строки имени схемы.</span><span class="sxs-lookup"><span data-stu-id="e1681-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="e1681-137">Если _lParam \* содержит более 50 имен схем, сообщение завершается ошибкой с возвращаемым значением **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="e1681-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1681-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1681-138">Remarks</span></span>

<span data-ttu-id="e1681-139">Если автоматическое обнаружение URL-адресов включено (т. е. *wParam* включает **аурл \_ енаблеурл**), элемент управления Rich Edit («Правка») сканирует любой измененный текст, чтобы определить, соответствует ли текст формату URL-адреса (или, как правило, в Windows 8 или более поздней версии для IRI международного идентификатора ресурса).</span><span class="sxs-lookup"><span data-stu-id="e1681-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="e1681-140">Если параметр *lParam* имеет значение null, элемент управления обнаруживает URL-адреса, начинающиеся со следующих имен схем:</span><span class="sxs-lookup"><span data-stu-id="e1681-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="e1681-141">callto</span><span class="sxs-lookup"><span data-stu-id="e1681-141">callto</span></span>
-   <span data-ttu-id="e1681-142">файл</span><span class="sxs-lookup"><span data-stu-id="e1681-142">file</span></span>
-   <span data-ttu-id="e1681-143">ftp</span><span class="sxs-lookup"><span data-stu-id="e1681-143">ftp</span></span>
-   <span data-ttu-id="e1681-144">gopher</span><span class="sxs-lookup"><span data-stu-id="e1681-144">gopher</span></span>
-   <span data-ttu-id="e1681-145">http</span><span class="sxs-lookup"><span data-stu-id="e1681-145">http</span></span>
-   <span data-ttu-id="e1681-146">HTTPS</span><span class="sxs-lookup"><span data-stu-id="e1681-146">https</span></span>
-   <span data-ttu-id="e1681-147">mailto</span><span class="sxs-lookup"><span data-stu-id="e1681-147">mailto</span></span>
-   <span data-ttu-id="e1681-148">news</span><span class="sxs-lookup"><span data-stu-id="e1681-148">news</span></span>
-   <span data-ttu-id="e1681-149">HDInsight</span><span class="sxs-lookup"><span data-stu-id="e1681-149">notes</span></span>
-   <span data-ttu-id="e1681-150">Разверните</span><span class="sxs-lookup"><span data-stu-id="e1681-150">nntp</span></span>
-   <span data-ttu-id="e1681-151">onenote</span><span class="sxs-lookup"><span data-stu-id="e1681-151">onenote</span></span>
-   <span data-ttu-id="e1681-152">outlook</span><span class="sxs-lookup"><span data-stu-id="e1681-152">outlook</span></span>
-   <span data-ttu-id="e1681-153">просперо</span><span class="sxs-lookup"><span data-stu-id="e1681-153">prospero</span></span>
-   <span data-ttu-id="e1681-154">tel</span><span class="sxs-lookup"><span data-stu-id="e1681-154">tel</span></span>
-   <span data-ttu-id="e1681-155">telnet</span><span class="sxs-lookup"><span data-stu-id="e1681-155">telnet</span></span>
-   <span data-ttu-id="e1681-156">wais</span><span class="sxs-lookup"><span data-stu-id="e1681-156">wais</span></span>
-   <span data-ttu-id="e1681-157">вебкал</span><span class="sxs-lookup"><span data-stu-id="e1681-157">webcal</span></span>

<span data-ttu-id="e1681-158">Если автоматическое обнаружение ссылок включено, элемент управления Rich Edit удаляет из измененного текста, который не распознается элементом управления, **CFE \_ связь** .</span><span class="sxs-lookup"><span data-stu-id="e1681-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="e1681-159">Если приложение использует **CFE \_ ссылку** для пометки других типов текста, не включайте автоматическое обнаружение ссылок.</span><span class="sxs-lookup"><span data-stu-id="e1681-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="e1681-160">Элемент управления Rich Edit не проверяет, существует ли обнаруженная ссылка; Эта ответственность принадлежит клиенту.</span><span class="sxs-lookup"><span data-stu-id="e1681-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="e1681-161">Форматированный элемент управления "поле ввода" отправляет уведомление [ \_ ссылки EN](en-link.md) при получении различных сообщений, в то время как указатель мыши находится над текстом, имеющим результат **CFE \_** .</span><span class="sxs-lookup"><span data-stu-id="e1681-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="e1681-162">Дополнительные сведения см. в разделе гиперссылки на [Автоматические гиперссылки](/archive/blogs/murrays/automatic-richedit-hyperlinks) и [понятное имя RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="e1681-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1681-163">Требования</span><span class="sxs-lookup"><span data-stu-id="e1681-163">Requirements</span></span>



| <span data-ttu-id="e1681-164">Требование</span><span class="sxs-lookup"><span data-stu-id="e1681-164">Requirement</span></span> | <span data-ttu-id="e1681-165">Значение</span><span class="sxs-lookup"><span data-stu-id="e1681-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1681-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1681-166">Minimum supported client</span></span><br/> | <span data-ttu-id="e1681-167">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1681-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1681-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1681-168">Minimum supported server</span></span><br/> | <span data-ttu-id="e1681-169">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1681-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1681-170">Header</span><span class="sxs-lookup"><span data-stu-id="e1681-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1681-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1681-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1681-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1681-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1681-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="e1681-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="e1681-174">\_ссылка EN</span><span class="sxs-lookup"><span data-stu-id="e1681-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 


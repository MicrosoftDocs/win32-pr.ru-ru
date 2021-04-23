---
title: Сообщение EM_STREAMOUT (RichEdit. h)
description: Заставляет форматированный элемент управления "поле ввода" передавать свое содержимое в приложение \ 8211; определенная функция обратного вызова Едитстреамкаллбакк. Затем функция обратного вызова может записать поток данных в файл или в любое другое выбранное расположение.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Элементы управления Windows для EM_STREAMOUT сообщений
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988696"
---
# <a name="em_streamout-message"></a><span data-ttu-id="3e843-105">\_Сообщение о потоке EM</span><span class="sxs-lookup"><span data-stu-id="3e843-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="3e843-106">Заставляет форматируемый элемент управления "поле ввода" передавать его содержимое в определенную приложением функцию обратного вызова [*едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) .</span><span class="sxs-lookup"><span data-stu-id="3e843-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="3e843-107">Затем функция обратного вызова может записать поток данных в файл или в любое другое выбранное расположение.</span><span class="sxs-lookup"><span data-stu-id="3e843-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e843-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e843-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e843-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e843-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e843-110">Задает формат данных и параметры замены.</span><span class="sxs-lookup"><span data-stu-id="3e843-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="3e843-111">Это значение должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3e843-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="3e843-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3e843-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3e843-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3e843-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="3e843-114"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="3e843-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="3e843-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="3e843-116"><dt>**SF \_ ртфнубжс**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="3e843-117">RTF с пробелами вместо COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="3e843-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="3e843-118"><dt>**\_текст**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="3e843-119">Текст с пробелами вместо COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="3e843-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="3e843-120"><dt>**с \_ текстом**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="3e843-121">Текст с текстовым представлением COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="3e843-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="3e843-122">Параметр **SF \_ ртфнубжс** полезен, если приложение хранит сами COM-объекты, так как представление RTF COM-объектов не очень компактно.</span><span class="sxs-lookup"><span data-stu-id="3e843-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="3e843-123">Управляющее слово, \\ обжаттф, за которым следует пробел, означает расположение объекта.</span><span class="sxs-lookup"><span data-stu-id="3e843-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="3e843-124">Кроме того, можно указать следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="3e843-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="3e843-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3e843-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="3e843-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3e843-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="3e843-127"><dt>**СФФ \_ плаинртф**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="3e843-128">Если этот параметр задан, элемент управления Rich Edit обрабатывает только ключевые слова, общие для всех языков, игнорируя ключевые слова, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="3e843-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="3e843-129">Если этот параметр не указан, элемент управления Rich Edit пересылает все ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="3e843-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="3e843-130">Этот флаг можно сочетать с флагом **SF \_ RTF** или **SF \_ ртфнубжс** .</span><span class="sxs-lookup"><span data-stu-id="3e843-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="3e843-131"><dt>**СФФ \_ Выбор**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="3e843-132">Если этот параметр задан, элемент управления Rich Edit создает потоковую передачу только содержимого текущего выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="3e843-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="3e843-133">Если не указано, элемент управления выдает все содержимое в потоке.</span><span class="sxs-lookup"><span data-stu-id="3e843-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="3e843-134">Этот флаг можно сочетать с любыми значениями формата данных.</span><span class="sxs-lookup"><span data-stu-id="3e843-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="3e843-135"><dt>**SF \_ Юникод**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="3e843-136">**Microsoft Rich Edit 2,0 и более поздние версии:** Указывает текст в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3e843-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="3e843-137">Этот флаг можно объединить с флагом **\_ текста** .</span><span class="sxs-lookup"><span data-stu-id="3e843-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="3e843-138"><dt>**SF \_ усекодепаже**</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="3e843-139">**Расширенное редактирование 3,0 и более поздних версий:** Создает RTF в формате UTF-8 и текст с помощью других кодовых страниц.</span><span class="sxs-lookup"><span data-stu-id="3e843-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="3e843-140">Кодовая страница задается в высоком слове *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3e843-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="3e843-141">Например, для UTF-8 RTF установите для параметра *wParam* значение (CP \_ UTF8 << 16) \| SF \_ \| \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="3e843-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="3e843-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e843-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e843-143">Указатель на структуру [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="3e843-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="3e843-144">На входе **пфнкаллбакк** член этой структуры должен указывать на приложение, определенную [*едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) функцию.</span><span class="sxs-lookup"><span data-stu-id="3e843-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="3e843-145">В выходных данных элемент **дверрор** может содержать ненулевой код ошибки, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3e843-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e843-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e843-146">Return value</span></span>

<span data-ttu-id="3e843-147">Это сообщение возвращает число символов, записанных в поток данных.</span><span class="sxs-lookup"><span data-stu-id="3e843-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e843-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e843-148">Remarks</span></span>

<span data-ttu-id="3e843-149">При отправке сообщения **о \_ потоке EM** элемент управления Rich Edit выполняет повторяющиеся вызовы функции [*едитстреамкаллбакк*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) , указанной членом **пфнкаллбакк** структуры [**едитстреам**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="3e843-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="3e843-150">Каждый раз при вызове функции обратного вызова элемент управления передает буфер, содержащий часть содержимого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3e843-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="3e843-151">Этот процесс будет продолжен до тех пор, пока элемент управления не перейдет все содержимое в функцию обратного вызова или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3e843-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e843-152">Требования</span><span class="sxs-lookup"><span data-stu-id="3e843-152">Requirements</span></span>



| <span data-ttu-id="3e843-153">Требование</span><span class="sxs-lookup"><span data-stu-id="3e843-153">Requirement</span></span> | <span data-ttu-id="3e843-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3e843-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e843-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e843-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3e843-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e843-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e843-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e843-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3e843-158">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e843-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e843-159">Header</span><span class="sxs-lookup"><span data-stu-id="3e843-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e843-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e843-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e843-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e843-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e843-162">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3e843-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e843-163">**едитстреам**</span><span class="sxs-lookup"><span data-stu-id="3e843-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="3e843-164">*едитстреамкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="3e843-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="3e843-165">**\_поток EM**</span><span class="sxs-lookup"><span data-stu-id="3e843-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 






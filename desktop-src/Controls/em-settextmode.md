---
title: Сообщение EM_SETTEXTMODE (RichEdit. h)
description: Задает режим текста или уровень отмены для элемента управления расширенного редактирования. Сообщение завершается ошибкой, если элемент управления содержит какой бы то ни было текст.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Элементы управления Windows для EM_SETTEXTMODE сообщений
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988822"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="f8a6b-105">\_Сообщение СЕТТЕКСТМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="f8a6b-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="f8a6b-106">Задает режим текста или уровень отмены для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="f8a6b-107">Сообщение завершается ошибкой, если элемент управления содержит какой бы то ни было текст.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8a6b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8a6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a6b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8a6b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a6b-110">Одно или несколько значений из типа перечисления [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="f8a6b-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="f8a6b-111">Значения указывают новые параметры для текстового режима элемента управления и параметры уровня отмены.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="f8a6b-112">Укажите одно из следующих значений, чтобы задать параметр текстового режима.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="f8a6b-113">Если не указать значение текстового режима, то текстовый режим останется в текущем параметре.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="f8a6b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-114">Value</span></span>                                          | <span data-ttu-id="f8a6b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8a6b-116">**\_открытый текст TM**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f8a6b-117">Указывает режим обычного текста, в котором элемент управления аналогичен стандартному элементу управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="f8a6b-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="f8a6b-118">Дополнительные сведения о режиме обычного текста см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f8a6b-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="f8a6b-119">**TM \_ RICHTEXT**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f8a6b-120">Указывает режим форматированного текста, в котором элемент управления имеет стандартные широкие возможности редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="f8a6b-121">Режим форматированного текста является параметром по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="f8a6b-122">Укажите одно из следующих значений, чтобы задать параметр уровня отмены.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="f8a6b-123">Если значение уровня отмены не задано, то уровень отмены остается в текущем параметре.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="f8a6b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-124">Value</span></span>                                                      | <span data-ttu-id="f8a6b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8a6b-126">**TM \_ синглелевелундо**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f8a6b-127">Элемент управления позволяет пользователю отменить только Последнее действие, которое может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="f8a6b-128">**TM \_ мултилевелундо**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f8a6b-129">Элемент управления поддерживает несколько операций отмены.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="f8a6b-130">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-130">This is the default setting.</span></span> <span data-ttu-id="f8a6b-131">Используйте сообщение [**EM \_ сетундолимит**](em-setundolimit.md) , чтобы задать максимальное количество действий отмены.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="f8a6b-132">Укажите одно из следующих значений, чтобы задать параметр кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="f8a6b-133">Если не указать значение кодовой страницы, то кодовая страница остается в текущем параметре.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="f8a6b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-134">Value</span></span>                                                    | <span data-ttu-id="f8a6b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8a6b-136">**TM \_ синглекодепаже**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f8a6b-137">Элемент управления допускает только английскую клавиатуру и клавиатуру, соответствующие кодировке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="f8a6b-138">Например, можно использовать греческий и английский язык.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="f8a6b-139">Обратите внимание, что это предотвращает ввод элемента управления в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="f8a6b-140">Например, используйте это значение, если элемент управления Rich Edit должен быть ограничен текстом ANSI.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="f8a6b-141">**\_МНОГОкодовая страница TM**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f8a6b-142">Элемент управления допускает в элементе управления несколько кодовых страниц и текста в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="f8a6b-143">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="f8a6b-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8a6b-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a6b-145">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a6b-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-146">Return value</span></span>

<span data-ttu-id="f8a6b-147">Если сообщение прошло удачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="f8a6b-148">Если сообщение не выполняется, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a6b-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8a6b-149">Remarks</span></span>

<span data-ttu-id="f8a6b-150">В режиме форматированного текста расширенный элемент управления "поле ввода" имеет стандартные широкие возможности редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="f8a6b-151">Однако в режиме обычного текста элемент управления аналогичен стандартному элементу управления Edit:</span><span class="sxs-lookup"><span data-stu-id="f8a6b-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="f8a6b-152">Текст в элементе управления обычным текстом может иметь только один формат (например, полужирный шрифт, 10 пт, Arial).</span><span class="sxs-lookup"><span data-stu-id="f8a6b-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="f8a6b-153">Пользователь не может вставлять форматированные текстовые форматы, такие как RTF или внедренные объекты, в обычный текстовый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="f8a6b-154">Элементы управления в режиме форматированного текста всегда имеют маркер конца документа по умолчанию или символ возврата каретки для форматирования абзацев.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="f8a6b-155">Элементы управления обычным текстом, с другой стороны, не нуждаются в маркере конца документа по умолчанию, поэтому он опускается.</span><span class="sxs-lookup"><span data-stu-id="f8a6b-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="f8a6b-156">Элемент управления не должен содержать текст при получении сообщения **EM \_ сеттекстмоде** .</span><span class="sxs-lookup"><span data-stu-id="f8a6b-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="f8a6b-157">Чтобы убедиться в отсутствии текста, отправьте сообщение [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) с пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="f8a6b-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a6b-158">Требования</span><span class="sxs-lookup"><span data-stu-id="f8a6b-158">Requirements</span></span>



| <span data-ttu-id="f8a6b-159">Требование</span><span class="sxs-lookup"><span data-stu-id="f8a6b-159">Requirement</span></span> | <span data-ttu-id="f8a6b-160">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a6b-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a6b-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8a6b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a6b-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8a6b-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8a6b-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8a6b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a6b-164">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8a6b-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8a6b-165">Header</span><span class="sxs-lookup"><span data-stu-id="f8a6b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a6b-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a6b-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a6b-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8a6b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a6b-168">**EM \_ жеттекстмоде**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="f8a6b-169">**EM \_ сетундолимит**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="f8a6b-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="f8a6b-171">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="f8a6b-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


---
title: Сообщение EM_SETWORDBREAKPROC (Winuser. h)
description: Заменяет функцию переносить по умолчанию элемента управления "Изменить" на определяемую приложением функцию переноса слов. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Элементы управления Windows для EM_SETWORDBREAKPROC сообщений
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534361"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="8d410-105">\_Сообщение СЕТВОРДБРЕАКПРОК EM</span><span class="sxs-lookup"><span data-stu-id="8d410-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="8d410-106">Заменяет функцию переносить по умолчанию элемента управления "Изменить" на определяемую приложением функцию переноса слов.</span><span class="sxs-lookup"><span data-stu-id="8d410-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="8d410-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8d410-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d410-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d410-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d410-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d410-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d410-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="8d410-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8d410-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d410-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d410-112">Адрес определяемой приложением функции WordWrap.</span><span class="sxs-lookup"><span data-stu-id="8d410-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="8d410-113">Дополнительные сведения о разбиении строк см. в описании функции обратного вызова [*едитвордбреакпрок*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="8d410-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d410-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d410-114">Return value</span></span>

<span data-ttu-id="8d410-115">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8d410-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d410-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d410-116">Remarks</span></span>

<span data-ttu-id="8d410-117">Функция WordWrap сканирует текстовый буфер, который содержит текст, отправляемый на экран, и ищет первое слово, не помещается на текущей линии экрана.</span><span class="sxs-lookup"><span data-stu-id="8d410-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="8d410-118">Функция WordWrap помещает это слово в начало следующей строки на экране.</span><span class="sxs-lookup"><span data-stu-id="8d410-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="8d410-119">Функция WordWrap определяет точку, в которой система должна разбивать строку текста для элементов управления многострочного редактирования, обычно в виде символа пробела, разделяющего два слова.</span><span class="sxs-lookup"><span data-stu-id="8d410-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="8d410-120">Однострочный или однострочный элемент управления "поле ввода" может вызывать эту функцию, когда пользователь нажимает клавиши со стрелками в сочетании с клавишей CTRL для перемещения курсора к следующему слову или предыдущему слову.</span><span class="sxs-lookup"><span data-stu-id="8d410-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="8d410-121">Функция WordWrap по умолчанию разбивает строку текста по символу пробела.</span><span class="sxs-lookup"><span data-stu-id="8d410-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="8d410-122">Определяемая приложением функция может определять переносить дефис или символ, отличный от символа пробела.</span><span class="sxs-lookup"><span data-stu-id="8d410-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="8d410-123">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8d410-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8d410-124">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8d410-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d410-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8d410-125">Requirements</span></span>



| <span data-ttu-id="8d410-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8d410-126">Requirement</span></span> | <span data-ttu-id="8d410-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8d410-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d410-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d410-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d410-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d410-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d410-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d410-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d410-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d410-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d410-132">Header</span><span class="sxs-lookup"><span data-stu-id="8d410-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d410-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d410-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d410-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d410-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d410-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8d410-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d410-136">*едитвордбреакпрок*</span><span class="sxs-lookup"><span data-stu-id="8d410-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="8d410-137">**EM \_ фмтлинес**</span><span class="sxs-lookup"><span data-stu-id="8d410-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="8d410-138">**EM \_ жетвордбреакпрок**</span><span class="sxs-lookup"><span data-stu-id="8d410-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 


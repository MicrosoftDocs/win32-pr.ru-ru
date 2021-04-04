---
title: Сообщение EM_SCROLL (Winuser. h)
description: Прокручивает текст по вертикали в многострочном элементе управления Edit. Это сообщение эквивалентно отправке сообщения WM \_ VSCROLL в элемент управления Edit. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Элементы управления Windows для EM_SCROLL сообщений
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137623"
---
# <a name="em_scroll-message"></a><span data-ttu-id="7a604-106">\_Сообщение с прокруткой EM</span><span class="sxs-lookup"><span data-stu-id="7a604-106">EM\_SCROLL message</span></span>

<span data-ttu-id="7a604-107">Прокручивает текст по вертикали в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="7a604-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="7a604-108">Это сообщение эквивалентно отправке сообщения [**WM \_ VSCROLL**](wm-vscroll.md) в элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="7a604-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="7a604-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="7a604-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a604-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a604-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a604-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a604-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a604-112">Действие, которое займет полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7a604-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="7a604-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="7a604-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7a604-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7a604-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="7a604-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7a604-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="7a604-116"><dt>**SB \_ линедовн**</dt></span><span class="sxs-lookup"><span data-stu-id="7a604-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="7a604-117">Выполняет прокрутку вниз на одну строку.</span><span class="sxs-lookup"><span data-stu-id="7a604-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="7a604-118"><dt>**построителя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a604-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="7a604-119">Выполняет прокрутку вверх на одну строку.</span><span class="sxs-lookup"><span data-stu-id="7a604-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="7a604-120"><dt>**SB \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="7a604-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="7a604-121">Выполняет прокрутку вниз на одну страницу.</span><span class="sxs-lookup"><span data-stu-id="7a604-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="7a604-122"><dt>**SB \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="7a604-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="7a604-123">Выполняет прокрутку вверх на одну страницу.</span><span class="sxs-lookup"><span data-stu-id="7a604-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7a604-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a604-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a604-125">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7a604-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a604-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a604-126">Return value</span></span>

<span data-ttu-id="7a604-127">Если сообщение прошло успешно, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) возвращает значение **true**, а [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — число строк, прокручиваемых командой.</span><span class="sxs-lookup"><span data-stu-id="7a604-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="7a604-128">Возвращаемое число может не совпадать с фактическим числом строк, прокручеясь, если прокрутка перемещается в начало или конец текста.</span><span class="sxs-lookup"><span data-stu-id="7a604-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="7a604-129">Если параметр *wParam* задает недопустимое значение, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="7a604-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a604-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a604-130">Remarks</span></span>

<span data-ttu-id="7a604-131">Для прокрутки до определенной позиции строки или символа используйте сообщение [**EM \_ линескролл**](em-linescroll.md) .</span><span class="sxs-lookup"><span data-stu-id="7a604-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="7a604-132">Чтобы прокрутить курсор на представление, используйте сообщение [**EM \_ скроллкарет**](em-scrollcaret.md) .</span><span class="sxs-lookup"><span data-stu-id="7a604-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="7a604-133">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="7a604-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7a604-134">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7a604-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a604-135">Требования</span><span class="sxs-lookup"><span data-stu-id="7a604-135">Requirements</span></span>



| <span data-ttu-id="7a604-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7a604-136">Requirement</span></span> | <span data-ttu-id="7a604-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7a604-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a604-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a604-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7a604-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a604-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a604-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a604-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7a604-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a604-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a604-142">Header</span><span class="sxs-lookup"><span data-stu-id="7a604-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a604-143"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a604-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a604-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a604-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a604-145">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7a604-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a604-146">**EM \_ линескролл**</span><span class="sxs-lookup"><span data-stu-id="7a604-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="7a604-147">**EM \_ скроллкарет**</span><span class="sxs-lookup"><span data-stu-id="7a604-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="7a604-148">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="7a604-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 


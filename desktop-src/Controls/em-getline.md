---
title: Сообщение EM_GETLINE (Winuser. h)
description: Копирует строку текста из элемента управления "поле ввода" и помещает ее в указанный буфер. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Элементы управления Windows для EM_GETLINE сообщений
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988272"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="e2079-105">Сообщение EM_GETLINE (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="e2079-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="e2079-106">Копирует строку текста из элемента управления "поле ввода" и помещает ее в указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="e2079-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="e2079-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e2079-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2079-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2079-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2079-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2079-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2079-110">Отсчитываемый от нуля индекс строки, извлекаемой из многострочного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e2079-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="e2079-111">Нулевое значение задает верхнюю строку.</span><span class="sxs-lookup"><span data-stu-id="e2079-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="e2079-112">Этот параметр игнорируется с помощью однострочного элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="e2079-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="e2079-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2079-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2079-114">Указатель на буфер, который получает копию строки.</span><span class="sxs-lookup"><span data-stu-id="e2079-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="e2079-115">Перед отправкой сообщения задайте для первого слова этого буфера размер буфера в **файле TCHAR**.</span><span class="sxs-lookup"><span data-stu-id="e2079-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="e2079-116">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="e2079-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="e2079-117">Размер в первом слове перезаписывается скопированной строкой.</span><span class="sxs-lookup"><span data-stu-id="e2079-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2079-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2079-118">Return value</span></span>

<span data-ttu-id="e2079-119">Возвращаемое значение — это число скопированных данных **TCHAR**.</span><span class="sxs-lookup"><span data-stu-id="e2079-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="e2079-120">Возвращаемое значение равно нулю, если номер строки, указанный параметром *wParam* , больше числа строк в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e2079-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2079-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2079-121">Remarks</span></span>

<span data-ttu-id="e2079-122">**Изменить элементы управления:** Скопированная строка не содержит завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="e2079-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="e2079-123">**Элементы управления Rich Edit:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e2079-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e2079-124">Скопированная строка не содержит завершающего нуль-символа, если текст не был скопирован.</span><span class="sxs-lookup"><span data-stu-id="e2079-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="e2079-125">Если текст не был скопирован, в начале буфера сообщения помещается символ null.</span><span class="sxs-lookup"><span data-stu-id="e2079-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="e2079-126">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e2079-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2079-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e2079-127">Requirements</span></span>



| <span data-ttu-id="e2079-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e2079-128">Requirement</span></span> | <span data-ttu-id="e2079-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e2079-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2079-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2079-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2079-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2079-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2079-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2079-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2079-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2079-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2079-134">Header</span><span class="sxs-lookup"><span data-stu-id="e2079-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2079-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2079-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2079-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2079-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2079-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e2079-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2079-138">**EM \_ линеленгс**</span><span class="sxs-lookup"><span data-stu-id="e2079-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="e2079-139">**Изменить \_ подстроку**</span><span class="sxs-lookup"><span data-stu-id="e2079-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="e2079-140">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e2079-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e2079-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="e2079-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 


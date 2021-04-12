---
title: Сообщение EM_LIMITTEXT (Winuser. h)
description: Задает ограничение текста для элемента управления "поле ввода".
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Элементы управления Windows для EM_LIMITTEXT сообщений
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489999"
---
# <a name="em_limittext-message"></a><span data-ttu-id="c8df4-104">\_Сообщение ЛИМИТТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="c8df4-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="c8df4-105">Задает ограничение текста для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8df4-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="c8df4-106">Ограничение текста — это максимальный объем текста в **файле TCHAR**, который пользователь может ввести в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8df4-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="c8df4-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c8df4-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="c8df4-108">Для элементов управления "поле ввода" и Microsoft Rich Editing 1,0 используются байты.</span><span class="sxs-lookup"><span data-stu-id="c8df4-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="c8df4-109">Для Microsoft Rich Edit 2,0 и более поздних версий используются символы.</span><span class="sxs-lookup"><span data-stu-id="c8df4-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8df4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8df4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8df4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8df4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8df4-112">Максимальное число записей **TCHAR**, которые может ввести пользователь.</span><span class="sxs-lookup"><span data-stu-id="c8df4-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="c8df4-113">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="c8df4-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="c8df4-114">Это число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="c8df4-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="c8df4-115">**Элементы управления Rich Edit:** Если этот параметр равен нулю, длина текста задается равным 64 000 символам.</span><span class="sxs-lookup"><span data-stu-id="c8df4-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="c8df4-116">Если этот параметр равен нулю, то длина текста устанавливается в 0x7FFFFFFE символов для однострочных элементов управления редактирования или-1 для многострочных элементов управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="c8df4-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="c8df4-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8df4-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8df4-118">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c8df4-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8df4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8df4-119">Return value</span></span>

<span data-ttu-id="c8df4-120">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c8df4-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8df4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8df4-121">Remarks</span></span>

<span data-ttu-id="c8df4-122">Сообщение **EM \_ лимиттекст** ограничивает только текст, который может ввести пользователь.</span><span class="sxs-lookup"><span data-stu-id="c8df4-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="c8df4-123">Он не влияет на текст, который уже находится в элементе управления "поле ввода" при отправке сообщения, и на длину текста, скопированного в элемент управления "поле ввода" с помощью сообщения [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="c8df4-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="c8df4-124">Если приложение использует сообщение **WM \_ SETTEXT** для размещения большего текста в элементе управления "поле ввода", чем указано в **сообщении \_ лимиттекст EM** , пользователь может изменить все содержимое элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8df4-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="c8df4-125">Перед вызовом **EM \_ лимиттекст** ограничение по умолчанию для объема текста, которое пользователь может ввести в поле ввода, — 32 767 символов.</span><span class="sxs-lookup"><span data-stu-id="c8df4-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="c8df4-126">Для однострочных элементов управления редактирования ограничением текста является либо 0x7FFFFFFE байт, либо значение параметра *wParam* , в зависимости от того, что меньше.</span><span class="sxs-lookup"><span data-stu-id="c8df4-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="c8df4-127">Для многострочных элементов управления Edit это значение равно 1 байту или значению параметра *wParam* , в зависимости от того, какое значение меньше.</span><span class="sxs-lookup"><span data-stu-id="c8df4-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="c8df4-128">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c8df4-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c8df4-129">Используйте сообщение [**EM \_ екслимиттекст**](em-exlimittext.md) для значений длины текста, превышающих 64 000.</span><span class="sxs-lookup"><span data-stu-id="c8df4-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="c8df4-130">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c8df4-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8df4-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c8df4-131">Requirements</span></span>



| <span data-ttu-id="c8df4-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c8df4-132">Requirement</span></span> | <span data-ttu-id="c8df4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c8df4-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8df4-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8df4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c8df4-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8df4-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8df4-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8df4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c8df4-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8df4-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8df4-138">Header</span><span class="sxs-lookup"><span data-stu-id="c8df4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8df4-139"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8df4-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8df4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8df4-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8df4-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c8df4-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8df4-142">**EM \_ екслимиттекст**</span><span class="sxs-lookup"><span data-stu-id="c8df4-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="c8df4-143">**Изменить \_ лимиттекст**</span><span class="sxs-lookup"><span data-stu-id="c8df4-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="c8df4-144">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c8df4-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c8df4-145">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="c8df4-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


---
title: Сообщение EM_SETLIMITTEXT (Winuser. h)
description: Задает ограничение текста для элемента управления "поле ввода".
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Элементы управления Windows для EM_SETLIMITTEXT сообщений
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802656"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="fcc35-104">\_Сообщение СЕТЛИМИТТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="fcc35-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="fcc35-105">Задает ограничение текста для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="fcc35-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="fcc35-106">Ограничение текста — это максимальный объем текста в **файле TCHAR**, который пользователь может ввести в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="fcc35-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="fcc35-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fcc35-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="fcc35-108">Для элементов управления "поле ввода" и Microsoft Rich Editing 1,0 используются байты.</span><span class="sxs-lookup"><span data-stu-id="fcc35-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="fcc35-109">Для Microsoft Rich Edit 2,0 и более поздних версий используются символы.</span><span class="sxs-lookup"><span data-stu-id="fcc35-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="fcc35-110">Сообщение **EM \_ сетлимиттекст** идентично сообщению [**\_ лимиттекст EM**](em-limittext.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc35-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcc35-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcc35-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc35-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcc35-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc35-113">Максимальное число записей **TCHAR**, которые может ввести пользователь.</span><span class="sxs-lookup"><span data-stu-id="fcc35-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="fcc35-114">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="fcc35-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="fcc35-115">Это число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="fcc35-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="fcc35-116">**Элементы управления Rich Edit:** Если этот параметр равен нулю, длина текста задается равным 64 000 символам.</span><span class="sxs-lookup"><span data-stu-id="fcc35-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="fcc35-117">Если этот параметр равен нулю, то длина текста устанавливается в 0x7FFFFFFE символов для однострочных элементов управления редактирования или 1 для многострочных элементов управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="fcc35-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="fcc35-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcc35-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc35-119">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fcc35-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc35-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcc35-120">Return value</span></span>

<span data-ttu-id="fcc35-121">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fcc35-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc35-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcc35-122">Remarks</span></span>

<span data-ttu-id="fcc35-123">Сообщение **EM \_ сетлимиттекст** ограничивает только текст, который может ввести пользователь.</span><span class="sxs-lookup"><span data-stu-id="fcc35-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="fcc35-124">Он не влияет на текст, который уже находится в элементе управления "поле ввода" при отправке сообщения, и на длину текста, скопированного в элемент управления "поле ввода" с помощью сообщения [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="fcc35-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="fcc35-125">Если приложение использует сообщение **WM \_ SETTEXT** для размещения большего текста в элементе управления "поле ввода", чем указано в **сообщении \_ сетлимиттекст EM** , пользователь может изменить все содержимое элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="fcc35-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="fcc35-126">Перед вызовом **EM \_ сетлимиттекст** ограничение по умолчанию для объема текста, которое пользователь может ввести в поле ввода, — 32 767 символов.</span><span class="sxs-lookup"><span data-stu-id="fcc35-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="fcc35-127">Для однострочных элементов управления редактирования ограничением текста является либо 0x7FFFFFFE байт, либо значение параметра *wParam* , в зависимости от того, что меньше.</span><span class="sxs-lookup"><span data-stu-id="fcc35-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="fcc35-128">Для элементов управления многострочного редактирования это значение равно 1 байтам или значению параметра *wParam* , в зависимости от того, какое значение меньше.</span><span class="sxs-lookup"><span data-stu-id="fcc35-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="fcc35-129">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fcc35-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fcc35-130">Используйте сообщение [**EM \_ екслимиттекст**](em-exlimittext.md) для значений длины текста, превышающих 64 000.</span><span class="sxs-lookup"><span data-stu-id="fcc35-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="fcc35-131">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fcc35-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc35-132">Требования</span><span class="sxs-lookup"><span data-stu-id="fcc35-132">Requirements</span></span>



| <span data-ttu-id="fcc35-133">Требование</span><span class="sxs-lookup"><span data-stu-id="fcc35-133">Requirement</span></span> | <span data-ttu-id="fcc35-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fcc35-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc35-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcc35-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc35-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcc35-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcc35-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcc35-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc35-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcc35-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcc35-139">Header</span><span class="sxs-lookup"><span data-stu-id="fcc35-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcc35-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcc35-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc35-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcc35-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc35-142">**EM \_ жетлимиттекст**</span><span class="sxs-lookup"><span data-stu-id="fcc35-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 


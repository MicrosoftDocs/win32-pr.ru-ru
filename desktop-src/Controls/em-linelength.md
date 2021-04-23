---
title: Сообщение EM_LINELENGTH (Winuser. h)
description: Извлекает длину строки в символах в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Элементы управления Windows для EM_LINELENGTH сообщений
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892397"
---
# <a name="em_linelength-message"></a><span data-ttu-id="a0b54-105">\_Сообщение ЛИНЕЛЕНГС EM</span><span class="sxs-lookup"><span data-stu-id="a0b54-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="a0b54-106">Извлекает длину строки в символах в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a0b54-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="a0b54-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a0b54-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0b54-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0b54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0b54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b54-110">Индекс символа в строке, длина которого должна быть получена.</span><span class="sxs-lookup"><span data-stu-id="a0b54-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="a0b54-111">Если этот параметр больше числа символов в элементе управления, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a0b54-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="a0b54-112">Этот параметр может быть равен-1.</span><span class="sxs-lookup"><span data-stu-id="a0b54-112">This parameter can be -1.</span></span> <span data-ttu-id="a0b54-113">В этом случае сообщение возвращает число невыбранных символов в строках, содержащих выбранные символы.</span><span class="sxs-lookup"><span data-stu-id="a0b54-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="a0b54-114">Например, если выделение, расширенное от четвертого символа одной строки до восьмого символа от конца следующей строки, возвращаемое значение будет равно 10 (три символа в первой строке и семь на следующем).</span><span class="sxs-lookup"><span data-stu-id="a0b54-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="a0b54-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0b54-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b54-116">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a0b54-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b54-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0b54-117">Return value</span></span>

<span data-ttu-id="a0b54-118">Для элементов управления многострочного редактирования возвращаемое значение является длиной в **TCHAR** s строки, заданной параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a0b54-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="a0b54-119">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="a0b54-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="a0b54-120">Он не включает символ возврата каретки в конце строки.</span><span class="sxs-lookup"><span data-stu-id="a0b54-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="a0b54-121">Для однострочных элементов управления редактирования возвращаемое значение является длиной в **TCHAR** s текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a0b54-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="a0b54-122">Если параметр *wParam* больше числа символов в элементе управления, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a0b54-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b54-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0b54-123">Remarks</span></span>

<span data-ttu-id="a0b54-124">Используйте сообщение [**EM \_ линеиндекс**](em-lineindex.md) , чтобы получить индекс символа для заданного номера строки в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="a0b54-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="a0b54-125">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a0b54-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a0b54-126">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a0b54-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b54-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a0b54-127">Requirements</span></span>



| <span data-ttu-id="a0b54-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a0b54-128">Requirement</span></span> | <span data-ttu-id="a0b54-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a0b54-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b54-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0b54-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b54-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0b54-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0b54-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0b54-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b54-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0b54-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0b54-134">Header</span><span class="sxs-lookup"><span data-stu-id="a0b54-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b54-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b54-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b54-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0b54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b54-137">**EM \_ линеиндекс**</span><span class="sxs-lookup"><span data-stu-id="a0b54-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 






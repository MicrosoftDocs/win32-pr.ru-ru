---
title: Сообщение EM_GETWORDBREAKPROC (Winuser. h)
description: Возвращает адрес текущей функции WordWrap. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Элементы управления Windows для EM_GETWORDBREAKPROC сообщений
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492000"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="51a3b-105">\_Сообщение ЖЕТВОРДБРЕАКПРОК EM</span><span class="sxs-lookup"><span data-stu-id="51a3b-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="51a3b-106">Возвращает адрес текущей функции WordWrap.</span><span class="sxs-lookup"><span data-stu-id="51a3b-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="51a3b-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="51a3b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51a3b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51a3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51a3b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a3b-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="51a3b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51a3b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51a3b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a3b-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="51a3b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a3b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51a3b-113">Return value</span></span>

<span data-ttu-id="51a3b-114">Возвращаемое значение указывает адрес функции WordWrap, определяемой приложением.</span><span class="sxs-lookup"><span data-stu-id="51a3b-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="51a3b-115">Если функция WordWrap не существует, возвращается значение **null** .</span><span class="sxs-lookup"><span data-stu-id="51a3b-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a3b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51a3b-116">Remarks</span></span>

<span data-ttu-id="51a3b-117">Функция WordWrap сканирует текстовый буфер, содержащий текст, который должен быть отправлен на экран, с поиском первого слова, которое не умещается на текущей линии вывода.</span><span class="sxs-lookup"><span data-stu-id="51a3b-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="51a3b-118">Функция WordWrap помещает это слово в начало следующей строки на экране.</span><span class="sxs-lookup"><span data-stu-id="51a3b-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="51a3b-119">Функция WordWrap определяет точку, в которой система должна разбивать строку текста для элементов управления многострочного редактирования, обычно в виде символа пробела, разделяющего два слова.</span><span class="sxs-lookup"><span data-stu-id="51a3b-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="51a3b-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="51a3b-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="51a3b-121">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="51a3b-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51a3b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="51a3b-122">Requirements</span></span>



| <span data-ttu-id="51a3b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="51a3b-123">Requirement</span></span> | <span data-ttu-id="51a3b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="51a3b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a3b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51a3b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="51a3b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51a3b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51a3b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51a3b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="51a3b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51a3b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51a3b-129">Header</span><span class="sxs-lookup"><span data-stu-id="51a3b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="51a3b-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51a3b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51a3b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51a3b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="51a3b-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="51a3b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51a3b-133">*едитвордбреакпрок*</span><span class="sxs-lookup"><span data-stu-id="51a3b-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="51a3b-134">**EM \_ фмтлинес**</span><span class="sxs-lookup"><span data-stu-id="51a3b-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="51a3b-135">**EM \_ сетвордбреакпрок**</span><span class="sxs-lookup"><span data-stu-id="51a3b-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 


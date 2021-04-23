---
title: Сообщение EM_GETLIMITTEXT (Winuser. h)
description: Возвращает текущее ограничение текста для элемента управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Элементы управления Windows для EM_GETLIMITTEXT сообщений
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891513"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="ded3b-105">\_Сообщение ЖЕТЛИМИТТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="ded3b-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="ded3b-106">Возвращает текущее ограничение текста для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="ded3b-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="ded3b-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ded3b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ded3b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ded3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ded3b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ded3b-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ded3b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ded3b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ded3b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ded3b-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ded3b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded3b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ded3b-113">Return value</span></span>

<span data-ttu-id="ded3b-114">Возвращаемое значение — это ограничение текста.</span><span class="sxs-lookup"><span data-stu-id="ded3b-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded3b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ded3b-115">Remarks</span></span>

<span data-ttu-id="ded3b-116">**Изменение элементов управления, форматированное изменение 2,0 и более поздние версии:** Ограничение текста — это максимальный объем текста в **файле TCHAR**, который может содержать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ded3b-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="ded3b-117">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="ded3b-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="ded3b-118">Два документа с одинаковым ограничением на количество символов выдают одинаковый размер текста, даже если один из них имеет значение ANSI, а другой — в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="ded3b-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="ded3b-119">**Расширенное редактирование 1,0:** Ограничение текста — это максимальный объем текста в байтах, который может содержаться в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ded3b-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="ded3b-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ded3b-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ded3b-121">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ded3b-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ded3b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ded3b-122">Requirements</span></span>



| <span data-ttu-id="ded3b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ded3b-123">Requirement</span></span> | <span data-ttu-id="ded3b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ded3b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ded3b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ded3b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ded3b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ded3b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ded3b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ded3b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ded3b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ded3b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ded3b-129">Header</span><span class="sxs-lookup"><span data-stu-id="ded3b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded3b-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ded3b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded3b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ded3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded3b-132">**EM \_ сетлимиттекст**</span><span class="sxs-lookup"><span data-stu-id="ded3b-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 






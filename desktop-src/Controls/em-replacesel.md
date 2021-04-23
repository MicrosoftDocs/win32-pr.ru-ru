---
title: Сообщение EM_REPLACESEL (Winuser. h)
description: Заменяет выбранный текст в элементе управления "поле ввода" или элементе управления Rich Edit указанным текстом.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Элементы управления Windows для EM_REPLACESEL сообщений
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137626"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="522f2-104">\_Сообщение РЕПЛАЦЕСЕЛ EM</span><span class="sxs-lookup"><span data-stu-id="522f2-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="522f2-105">Заменяет выбранный текст в элементе управления "поле ввода" или элементе управления Rich Edit указанным текстом.</span><span class="sxs-lookup"><span data-stu-id="522f2-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="522f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="522f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="522f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="522f2-108">Указывает, можно ли отменить операцию замены.</span><span class="sxs-lookup"><span data-stu-id="522f2-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="522f2-109">Если это **так**, операция может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="522f2-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="522f2-110">Если это **значение равно false** , операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="522f2-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="522f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="522f2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="522f2-112">Указатель на строку с завершающим нулем, содержащую замещающий текст.</span><span class="sxs-lookup"><span data-stu-id="522f2-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522f2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="522f2-113">Return value</span></span>

<span data-ttu-id="522f2-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="522f2-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="522f2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="522f2-115">Remarks</span></span>

<span data-ttu-id="522f2-116">Используйте сообщение **EM \_ реплацесел** , чтобы заменить только часть текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="522f2-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="522f2-117">Чтобы заменить весь текст, используйте сообщение [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="522f2-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="522f2-118">Если ничего не выделено, замещающий текст вставляется в курсор.</span><span class="sxs-lookup"><span data-stu-id="522f2-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="522f2-119">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="522f2-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="522f2-120">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="522f2-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="522f2-121">В элементе управления для редактирования текста замещающий текст принимает форматирование символа в курсоре или, если имеется выделенный фрагмент, первого символа в выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="522f2-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="522f2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="522f2-122">Requirements</span></span>



| <span data-ttu-id="522f2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="522f2-123">Requirement</span></span> | <span data-ttu-id="522f2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="522f2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="522f2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="522f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="522f2-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="522f2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="522f2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="522f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="522f2-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="522f2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="522f2-129">Header</span><span class="sxs-lookup"><span data-stu-id="522f2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="522f2-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="522f2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522f2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="522f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522f2-132">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="522f2-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


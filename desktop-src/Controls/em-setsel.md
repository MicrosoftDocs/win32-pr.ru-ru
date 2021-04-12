---
title: Сообщение EM_SETSEL (Winuser. h)
description: Выбирает диапазон символов в элементе управления "изменение". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Элементы управления Windows для EM_SETSEL сообщений
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489990"
---
# <a name="em_setsel-message"></a><span data-ttu-id="c3b21-105">\_Сообщение СЕТСЕЛ EM</span><span class="sxs-lookup"><span data-stu-id="c3b21-105">EM\_SETSEL message</span></span>

<span data-ttu-id="c3b21-106">Выбирает диапазон символов в элементе управления "изменение".</span><span class="sxs-lookup"><span data-stu-id="c3b21-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="c3b21-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c3b21-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3b21-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3b21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3b21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3b21-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b21-110">Начальная позиции символа выделения.</span><span class="sxs-lookup"><span data-stu-id="c3b21-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="c3b21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3b21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b21-112">Позиция конечного символа выделения.</span><span class="sxs-lookup"><span data-stu-id="c3b21-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3b21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3b21-113">Return value</span></span>

<span data-ttu-id="c3b21-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c3b21-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b21-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3b21-115">Remarks</span></span>

<span data-ttu-id="c3b21-116">Начальное значение может быть больше, чем конечное значение.</span><span class="sxs-lookup"><span data-stu-id="c3b21-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="c3b21-117">В нижней части этих двух значений задается символ позиции первого символа в выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="c3b21-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="c3b21-118">Более высокое значение задает позиции первого символа после выбора.</span><span class="sxs-lookup"><span data-stu-id="c3b21-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="c3b21-119">Начальное значение — это точка привязки выделения, а конечное значение — активный конец.</span><span class="sxs-lookup"><span data-stu-id="c3b21-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="c3b21-120">Если пользователь использует клавишу SHIFT для корректировки размера выделения, активная конечная точка может перемещаться, но точки привязки остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="c3b21-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="c3b21-121">Если начальное значение равно 0, а конец — 1, то выделяется весь текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c3b21-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="c3b21-122">Если значение Start равно-1, то все текущие выделения отменяются.</span><span class="sxs-lookup"><span data-stu-id="c3b21-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="c3b21-123">**Изменить элементы управления:** Элемент управления отображает мигающий курсор в конечной позиции независимо от относительных значений Start и End.</span><span class="sxs-lookup"><span data-stu-id="c3b21-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="c3b21-124">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c3b21-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c3b21-125">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c3b21-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="c3b21-126">Если элемент управления Edit имеет стиль [**\_ нохидесел**](edit-control-styles.md) , выделенный текст выделяется независимо от того, имеет ли элемент управления фокус.</span><span class="sxs-lookup"><span data-stu-id="c3b21-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="c3b21-127">Без стиля **\_ нохидесел** выделенный текст выделяется только в том случае, если фокус находится на элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c3b21-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b21-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c3b21-128">Requirements</span></span>



| <span data-ttu-id="c3b21-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c3b21-129">Requirement</span></span> | <span data-ttu-id="c3b21-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c3b21-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b21-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3b21-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b21-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3b21-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c3b21-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3b21-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b21-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3b21-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c3b21-135">Header</span><span class="sxs-lookup"><span data-stu-id="c3b21-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3b21-136"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3b21-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b21-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3b21-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3b21-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c3b21-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3b21-139">**EM \_ жетсел**</span><span class="sxs-lookup"><span data-stu-id="c3b21-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="c3b21-140">**EM \_ реплацесел**</span><span class="sxs-lookup"><span data-stu-id="c3b21-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="c3b21-141">**EM \_ скроллкарет**</span><span class="sxs-lookup"><span data-stu-id="c3b21-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="c3b21-142">**EM \_ екссетсел**</span><span class="sxs-lookup"><span data-stu-id="c3b21-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 






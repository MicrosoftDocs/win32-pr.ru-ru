---
title: Сообщение EM_EMPTYUNDOBUFFER (Winuser. h)
description: Сбрасывает флаг отмены для элемента управления "поле ввода". Флаг отмены задается каждый раз, когда операция в элементе управления "поле ввода" может быть отменена. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Элементы управления Windows для EM_EMPTYUNDOBUFFER сообщений
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491496"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="b377f-106">\_Сообщение ЕМПТЮНДОБУФФЕР EM</span><span class="sxs-lookup"><span data-stu-id="b377f-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="b377f-107">Сбрасывает флаг отмены для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="b377f-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="b377f-108">Флаг отмены задается каждый раз, когда операция в элементе управления "поле ввода" может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="b377f-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="b377f-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b377f-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b377f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b377f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b377f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b377f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b377f-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b377f-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b377f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b377f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b377f-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b377f-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b377f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b377f-115">Return value</span></span>

<span data-ttu-id="b377f-116">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b377f-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b377f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b377f-117">Remarks</span></span>

<span data-ttu-id="b377f-118">Флаг отмены автоматически сбрасывается каждый раз, когда элемент управления "поле ввода" получает сообщение [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) или [**EM \_ сесандле**](em-sethandle.md) .</span><span class="sxs-lookup"><span data-stu-id="b377f-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="b377f-119">**Изменение элементов управления и форматированное изменение 1,0:** Элемент управления может только отменить или повторить последнюю операцию.</span><span class="sxs-lookup"><span data-stu-id="b377f-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="b377f-120">**Расширенное редактирование 2,0 и более поздних версий:** Сообщение **\_ емптюндобуффер EM** очищает все буферы отмены и повтора.</span><span class="sxs-lookup"><span data-stu-id="b377f-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="b377f-121">Элементы управления Rich Edit позволяют пользователю отменить или повторить несколько операций.</span><span class="sxs-lookup"><span data-stu-id="b377f-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="b377f-122">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b377f-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b377f-123">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b377f-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b377f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b377f-124">Requirements</span></span>



| <span data-ttu-id="b377f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b377f-125">Requirement</span></span> | <span data-ttu-id="b377f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b377f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b377f-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b377f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b377f-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b377f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b377f-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b377f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b377f-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b377f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b377f-131">Header</span><span class="sxs-lookup"><span data-stu-id="b377f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b377f-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b377f-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b377f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b377f-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="b377f-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b377f-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b377f-135">**EM \_ канундо**</span><span class="sxs-lookup"><span data-stu-id="b377f-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="b377f-136">**EM \_ сесандле**</span><span class="sxs-lookup"><span data-stu-id="b377f-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="b377f-137">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="b377f-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="b377f-138">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b377f-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b377f-139">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b377f-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


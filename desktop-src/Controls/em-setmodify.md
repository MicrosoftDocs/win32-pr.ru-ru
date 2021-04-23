---
title: Сообщение EM_SETMODIFY (Winuser. h)
description: Задает или очищает флаг изменения для элемента управления "поле ввода". Флаг изменения указывает, был ли изменен текст в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Элементы управления Windows для EM_SETMODIFY сообщений
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892161"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="51a1e-106">\_Сообщение СЕТМОДИФИ EM</span><span class="sxs-lookup"><span data-stu-id="51a1e-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="51a1e-107">Задает или очищает флаг изменения для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="51a1e-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="51a1e-108">Флаг изменения указывает, был ли изменен текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="51a1e-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="51a1e-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="51a1e-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51a1e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="51a1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a1e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51a1e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a1e-112">Новое значение для флага изменения.</span><span class="sxs-lookup"><span data-stu-id="51a1e-112">The new value for the modification flag.</span></span> <span data-ttu-id="51a1e-113">Значение **true** указывает, что текст был изменен, а значение **false** указывает, что он не был изменен.</span><span class="sxs-lookup"><span data-stu-id="51a1e-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="51a1e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51a1e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a1e-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="51a1e-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a1e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51a1e-116">Return value</span></span>

<span data-ttu-id="51a1e-117">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="51a1e-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a1e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51a1e-118">Remarks</span></span>

<span data-ttu-id="51a1e-119">При создании элемента управления система автоматически очищает флаг изменения до нуля.</span><span class="sxs-lookup"><span data-stu-id="51a1e-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="51a1e-120">Если пользователь изменяет текст элемента управления, система устанавливает флаг в значение ненулевой.</span><span class="sxs-lookup"><span data-stu-id="51a1e-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="51a1e-121">Чтобы получить текущее состояние флага, можно отправить сообщение [**EM \_**](em-getmodify.md) в элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="51a1e-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="51a1e-122">**Расширенное редактирование 1,0:** Объекты, созданные без флага **Рео \_ динамиксизе** , будут заблокированы в своих экстентах, если флаг Modify имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="51a1e-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="51a1e-123">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="51a1e-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="51a1e-124">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="51a1e-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51a1e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="51a1e-125">Requirements</span></span>



| <span data-ttu-id="51a1e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="51a1e-126">Requirement</span></span> | <span data-ttu-id="51a1e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="51a1e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a1e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51a1e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="51a1e-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51a1e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51a1e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51a1e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="51a1e-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51a1e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51a1e-132">Header</span><span class="sxs-lookup"><span data-stu-id="51a1e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="51a1e-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51a1e-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51a1e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51a1e-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="51a1e-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="51a1e-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51a1e-136">**EM, \_ изменение**</span><span class="sxs-lookup"><span data-stu-id="51a1e-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="51a1e-137">**Переобъектировать**</span><span class="sxs-lookup"><span data-stu-id="51a1e-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 






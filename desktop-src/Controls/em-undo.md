---
title: Сообщение EM_UNDO (Winuser. h)
description: Это сообщение отменяет последнюю операцию редактирования элемента управления в очереди отмены элемента управления. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Элементы управления Windows для EM_UNDO сообщений
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802333"
---
# <a name="em_undo-message"></a><span data-ttu-id="452b0-105">\_Сообщение об отмене EM</span><span class="sxs-lookup"><span data-stu-id="452b0-105">EM\_UNDO message</span></span>

<span data-ttu-id="452b0-106">Это сообщение отменяет последнюю операцию редактирования элемента управления в очереди отмены элемента управления.</span><span class="sxs-lookup"><span data-stu-id="452b0-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="452b0-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="452b0-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="452b0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="452b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="452b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="452b0-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="452b0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="452b0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="452b0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="452b0-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="452b0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452b0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="452b0-113">Return value</span></span>

<span data-ttu-id="452b0-114">Для элемента управления "поле ввода с одной строкой" возвращаемое значение всегда равно **true**.</span><span class="sxs-lookup"><span data-stu-id="452b0-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="452b0-115">Для многострочного элемента управления "поле ввода" возвращаемое значение равно **true** , если операция отмены выполнена успешно, или **значение false** , если операция отмены завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="452b0-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="452b0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="452b0-116">Remarks</span></span>

<span data-ttu-id="452b0-117">**Изменение элементов управления и форматированное изменение 1,0:** Операция отмены также может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="452b0-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="452b0-118">Например, можно восстановить удаленный текст с первым сообщением о возврате EM и удалить его еще раз со вторым сообщением **\_ отмены EM** при условии отсутствия промежуточной операции редактирования. **\_**</span><span class="sxs-lookup"><span data-stu-id="452b0-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="452b0-119">**Расширенное редактирование 2,0 и более поздних версий:** Функция отмены является многоуровневой, поэтому отправка двух сообщений **\_ отмены EM** приведет к отмене последних двух операций в очереди отмены.</span><span class="sxs-lookup"><span data-stu-id="452b0-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="452b0-120">Чтобы повторить операцию, отправьте сообщение о [**\_ возврате EM**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="452b0-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="452b0-121">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="452b0-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="452b0-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="452b0-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="452b0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="452b0-123">Requirements</span></span>



| <span data-ttu-id="452b0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="452b0-124">Requirement</span></span> | <span data-ttu-id="452b0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="452b0-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="452b0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="452b0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="452b0-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="452b0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="452b0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="452b0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="452b0-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="452b0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="452b0-130">Header</span><span class="sxs-lookup"><span data-stu-id="452b0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="452b0-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="452b0-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452b0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="452b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452b0-133">**EM \_ канундо**</span><span class="sxs-lookup"><span data-stu-id="452b0-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 






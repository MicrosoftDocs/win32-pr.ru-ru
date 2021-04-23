---
title: Сообщение EM_CANUNDO (Winuser. h)
description: Определяет, существуют ли какие либо действия в очереди отмены элемента управления "изменение". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Элементы управления Windows для EM_CANUNDO сообщений
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136447"
---
# <a name="em_canundo-message"></a><span data-ttu-id="1094e-105">\_Сообщение КАНУНДО EM</span><span class="sxs-lookup"><span data-stu-id="1094e-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="1094e-106">Определяет, существуют ли какие либо действия в очереди отмены элемента управления "изменение".</span><span class="sxs-lookup"><span data-stu-id="1094e-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="1094e-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1094e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1094e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1094e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1094e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1094e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1094e-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1094e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1094e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1094e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1094e-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1094e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1094e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1094e-113">Return value</span></span>

<span data-ttu-id="1094e-114">Если в очереди отмены элемента управления есть действия, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1094e-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="1094e-115">Если очередь отмены пуста, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1094e-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1094e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1094e-116">Remarks</span></span>

<span data-ttu-id="1094e-117">Если очередь отмены не пуста, можно отправить сообщение об [**\_ отмене EM**](em-undo.md) в элемент управления, чтобы отменить самую последнюю операцию.</span><span class="sxs-lookup"><span data-stu-id="1094e-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="1094e-118">**Изменение элементов управления и форматированное изменение 1,0:** Очередь отмены содержит только последнюю операцию.</span><span class="sxs-lookup"><span data-stu-id="1094e-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="1094e-119">**Расширенное редактирование 2,0 и более поздних версий:** Очередь отмены может содержать несколько операций.</span><span class="sxs-lookup"><span data-stu-id="1094e-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="1094e-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1094e-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1094e-121">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1094e-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1094e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1094e-122">Requirements</span></span>



| <span data-ttu-id="1094e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1094e-123">Requirement</span></span> | <span data-ttu-id="1094e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1094e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1094e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1094e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1094e-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1094e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1094e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1094e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1094e-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1094e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1094e-129">Header</span><span class="sxs-lookup"><span data-stu-id="1094e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1094e-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1094e-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1094e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1094e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1094e-132">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="1094e-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 






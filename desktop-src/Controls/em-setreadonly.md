---
title: Сообщение EM_SETREADONLY (Winuser. h)
description: Задает или удаляет доступный только для чтения стиль ( \_ ReadOnly) элемента управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Элементы управления Windows для EM_SETREADONLY сообщений
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135787"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="46c28-105">\_Сообщение SETREADONLY EM</span><span class="sxs-lookup"><span data-stu-id="46c28-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="46c28-106">Задает или удаляет доступный только для чтения стиль ([**\_ ReadOnly**](edit-control-styles.md)) элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="46c28-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="46c28-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="46c28-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="46c28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46c28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c28-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46c28-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46c28-110">Указывает, следует ли устанавливать или удалять [**стиль \_ только для чтения ES**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="46c28-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="46c28-111">Значение **true** задает стиль, **\_ доступный только для чтения** и т. е. значение **false** удаляет стиль **\_ только для чтения** .</span><span class="sxs-lookup"><span data-stu-id="46c28-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="46c28-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46c28-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46c28-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="46c28-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c28-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46c28-114">Return value</span></span>

<span data-ttu-id="46c28-115">Если операция выполнена удачно, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="46c28-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="46c28-116">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="46c28-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="46c28-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46c28-117">Remarks</span></span>

<span data-ttu-id="46c28-118">Если элемент управления "поле ввода" имеет стиль " [**\_ только для чтения**](edit-control-styles.md) ", пользователь не может изменить текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="46c28-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="46c28-119">Чтобы определить, имеет ли элемент управления "поле ввода" стиль " [**\_ только для чтения**](edit-control-styles.md) ", используйте функцию [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) с \_ флагом стиля ГВЛ.</span><span class="sxs-lookup"><span data-stu-id="46c28-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="46c28-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="46c28-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="46c28-121">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="46c28-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46c28-122">Требования</span><span class="sxs-lookup"><span data-stu-id="46c28-122">Requirements</span></span>



| <span data-ttu-id="46c28-123">Требование</span><span class="sxs-lookup"><span data-stu-id="46c28-123">Requirement</span></span> | <span data-ttu-id="46c28-124">Значение</span><span class="sxs-lookup"><span data-stu-id="46c28-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c28-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46c28-125">Minimum supported client</span></span><br/> | <span data-ttu-id="46c28-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46c28-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46c28-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46c28-127">Minimum supported server</span></span><br/> | <span data-ttu-id="46c28-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46c28-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46c28-129">Header</span><span class="sxs-lookup"><span data-stu-id="46c28-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c28-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46c28-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c28-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46c28-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c28-132">**жетвиндовлонг**</span><span class="sxs-lookup"><span data-stu-id="46c28-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 


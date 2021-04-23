---
title: Сообщение EM_GETMODIFY (Winuser. h)
description: Возвращает состояние флага изменения элемента управления Edit. Флаг указывает, было ли изменено содержимое элемента управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Элементы управления Windows для EM_GETMODIFY сообщений
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891557"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="c4001-106">Сообщение EM при \_ изменении</span><span class="sxs-lookup"><span data-stu-id="c4001-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="c4001-107">Возвращает состояние флага изменения элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c4001-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="c4001-108">Флаг указывает, было ли изменено содержимое элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c4001-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="c4001-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c4001-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4001-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4001-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4001-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4001-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4001-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c4001-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4001-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4001-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4001-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c4001-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4001-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4001-115">Return value</span></span>

<span data-ttu-id="c4001-116">Если содержимое элемента управления "поле ввода" было изменено, возвращаемое значение не равно нулю; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c4001-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4001-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4001-117">Remarks</span></span>

<span data-ttu-id="c4001-118">При создании элемента управления система автоматически очищает флаг изменения до нуля.</span><span class="sxs-lookup"><span data-stu-id="c4001-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="c4001-119">Если пользователь изменяет текст элемента управления, система устанавливает флаг в значение ненулевой.</span><span class="sxs-lookup"><span data-stu-id="c4001-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="c4001-120">Сообщение [**EM \_ сетмодифи**](em-setmodify.md) можно отправить в элемент управления Правка, чтобы установить или снять флажок.</span><span class="sxs-lookup"><span data-stu-id="c4001-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="c4001-121">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c4001-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c4001-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c4001-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4001-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c4001-123">Requirements</span></span>



| <span data-ttu-id="c4001-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c4001-124">Requirement</span></span> | <span data-ttu-id="c4001-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c4001-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4001-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4001-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4001-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4001-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4001-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4001-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4001-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4001-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4001-130">Header</span><span class="sxs-lookup"><span data-stu-id="c4001-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4001-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4001-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4001-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4001-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4001-133">**EM \_ сетмодифи**</span><span class="sxs-lookup"><span data-stu-id="c4001-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 






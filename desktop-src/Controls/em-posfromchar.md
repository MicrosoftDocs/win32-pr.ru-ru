---
title: Сообщение EM_POSFROMCHAR (Winuser. h)
description: Получает координаты клиентской области указанного символа в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Элементы управления Windows для EM_POSFROMCHAR сообщений
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534367"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="04a9c-105">\_Сообщение ПОСФРОМЧАР EM</span><span class="sxs-lookup"><span data-stu-id="04a9c-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="04a9c-106">Получает координаты клиентской области указанного символа в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="04a9c-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="04a9c-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="04a9c-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="04a9c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04a9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04a9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04a9c-110">**Широкие возможности редактирования 1,0 и 3,0:** Указатель на [**точечную**](/previous-versions//dd162807(v=vs.85)) структуру, получающую координаты области клиента для символа.</span><span class="sxs-lookup"><span data-stu-id="04a9c-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="04a9c-111">Координаты находятся в единицах экрана и задаются относительно левого верхнего угла клиентской области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="04a9c-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="04a9c-112">**Изменение элементов управления и форматированное изменение 2,0:** Отсчитываемый от нуля индекс символа.</span><span class="sxs-lookup"><span data-stu-id="04a9c-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="04a9c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04a9c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04a9c-114">**Широкие возможности редактирования 1,0 и 3,0:** Отсчитываемый от нуля индекс символа.</span><span class="sxs-lookup"><span data-stu-id="04a9c-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="04a9c-115">**Изменение элементов управления и форматированное изменение 2,0:** Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="04a9c-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a9c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04a9c-116">Return value</span></span>

<span data-ttu-id="04a9c-117">**Широкие возможности редактирования 1,0 и 3,0:** Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="04a9c-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="04a9c-118">**Изменение элементов управления и форматированное изменение 2,0:** Возвращаемое значение содержит координаты клиентской области символа.</span><span class="sxs-lookup"><span data-stu-id="04a9c-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="04a9c-119">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит горизонтальную координату, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит вертикальную координату.</span><span class="sxs-lookup"><span data-stu-id="04a9c-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a9c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04a9c-120">Remarks</span></span>

<span data-ttu-id="04a9c-121">Возвращаемая координата может быть отрицательным значением, если указанный символ не отображается в клиентской области элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="04a9c-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="04a9c-122">Координаты усекаются до целых значений.</span><span class="sxs-lookup"><span data-stu-id="04a9c-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="04a9c-123">Если символ является разделителем строк, то возвращаемые координаты указывают на точку сразу за последним видимым символом в строке.</span><span class="sxs-lookup"><span data-stu-id="04a9c-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="04a9c-124">Если указанный индекс больше индекса последнего символа в элементе управления, элемент управления возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="04a9c-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="04a9c-125">**Расширенное редактирование 3,0 и более поздних версий:** Для обеспечения обратной совместимости Microsoft Rich Editing 3,0 поддерживает синтаксис, используемый Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="04a9c-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="04a9c-126">Если Microsoft Rich Edit 3,0 обнаружит, что параметр *wParam* не является [**допустимым**](/previous-versions//dd162807(v=vs.85)) указателем, предполагается, что сообщение было отправлено с помощью синтаксиса Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="04a9c-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="04a9c-127">В этом случае для возврата координат используется возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="04a9c-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="04a9c-128">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="04a9c-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="04a9c-129">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="04a9c-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04a9c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="04a9c-130">Requirements</span></span>



| <span data-ttu-id="04a9c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="04a9c-131">Requirement</span></span> | <span data-ttu-id="04a9c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="04a9c-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a9c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04a9c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="04a9c-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04a9c-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04a9c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04a9c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="04a9c-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04a9c-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04a9c-137">Header</span><span class="sxs-lookup"><span data-stu-id="04a9c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a9c-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04a9c-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a9c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04a9c-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="04a9c-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="04a9c-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04a9c-141">**EM \_ чарфромпос**</span><span class="sxs-lookup"><span data-stu-id="04a9c-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="04a9c-142">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="04a9c-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="04a9c-143">[**Точка зрения**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04a9c-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 


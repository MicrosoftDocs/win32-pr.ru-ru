---
title: Сообщение EM_SETRECT (Winuser. h)
description: EM_SETRECT сообщение — задает прямоугольник форматирования для многострочного элемента управления Edit.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Элементы управления Windows для EM_SETRECT сообщений
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085972"
---
# <a name="em_setrect-message"></a><span data-ttu-id="6d4a2-104">\_Сообщение SETRECT EM</span><span class="sxs-lookup"><span data-stu-id="6d4a2-104">EM\_SETRECT message</span></span>

<span data-ttu-id="6d4a2-105">Задает [прямоугольник форматирования](about-edit-controls.md) для многострочного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6d4a2-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="6d4a2-106">Прямоугольник форматирования — это ограничивающий прямоугольник, в который элемент управления рисует текст.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="6d4a2-107">Ограничивающий прямоугольник не зависит от размера окна элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6d4a2-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="6d4a2-108">Это сообщение обрабатывается только многострочными элементами управления Edit.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="6d4a2-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d4a2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d4a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4a2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d4a2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d4a2-112">**Расширенное редактирование 2,0 и более поздних версий:** Указывает, задает ли *lParam* абсолютные или относительные координаты.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="6d4a2-113">Нулевое значение обозначает абсолютные координаты.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="6d4a2-114">Значение 1 указывает смещения относительно текущего прямоугольника форматирования.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="6d4a2-115">(Смещение может быть положительным или отрицательным.)</span><span class="sxs-lookup"><span data-stu-id="6d4a2-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="6d4a2-116">**Изменение элементов управления и форматированное изменение 1,0:** Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6d4a2-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d4a2-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d4a2-118">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую новые размеры прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="6d4a2-119">Если этот параметр имеет **значение NULL**, то для прямоугольника форматирования задаются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4a2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d4a2-120">Return value</span></span>

<span data-ttu-id="6d4a2-121">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4a2-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="6d4a2-122">Remarks</span></span>

<span data-ttu-id="6d4a2-123">Установка параметра *lParam* в **значение NULL** не действует при установке сенсорного устройства или при отправке **EM \_ SETRECT** из потока с установленным обработчиком (см. раздел [**сетвиндовшукекс**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="6d4a2-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="6d4a2-124">В таких случаях *lParam* должен содержать допустимый указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6d4a2-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="6d4a2-125">Сообщение **EM \_ SETRECT** приводит к перерисовке текста элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6d4a2-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="6d4a2-126">Чтобы изменить размер прямоугольника форматирования без перерисовки текста, используйте сообщение [**EM \_ сетректнп**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="6d4a2-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="6d4a2-127">При первом создании элемента управления "поле ввода" для прямоугольника форматирования устанавливается размер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="6d4a2-128">Можно использовать сообщение **EM \_ SETRECT** , чтобы увеличить или уменьшить размер прямоугольника форматирования, чем окно элемента управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="6d4a2-129">Если элемент управления "поле ввода" не имеет горизонтальной полосы прокрутки, а размер прямоугольника форматирования больше окна элемента управления "поле ввода", строки текста, превышающие ширину окна элемента управления "поле ввода" (но меньше, чем ширина прямоугольника форматирования), обрезаются, а не упаковываются.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="6d4a2-130">Если элемент управления "поле ввода" содержит границу, размер прямоугольника форматирования уменьшается по размеру границы.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="6d4a2-131">Если вы настраиваете прямоугольник, возвращенный сообщением EM, необходимо удалить размер границы перед использованием прямоугольника с сообщением **EM \_ SETRECT** . [**\_**](em-getrect.md)</span><span class="sxs-lookup"><span data-stu-id="6d4a2-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="6d4a2-132">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6d4a2-133">Прямоугольник форматирования не включает панель выбора, которая является непомеченной областью слева от каждого абзаца.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="6d4a2-134">Когда пользователь щелкает на панели выбора, выбирается соответствующая строка.</span><span class="sxs-lookup"><span data-stu-id="6d4a2-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="6d4a2-135">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6d4a2-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4a2-136">Требования</span><span class="sxs-lookup"><span data-stu-id="6d4a2-136">Requirements</span></span>



| <span data-ttu-id="6d4a2-137">Требование</span><span class="sxs-lookup"><span data-stu-id="6d4a2-137">Requirement</span></span> | <span data-ttu-id="6d4a2-138">Значение</span><span class="sxs-lookup"><span data-stu-id="6d4a2-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4a2-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d4a2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4a2-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d4a2-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d4a2-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d4a2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4a2-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d4a2-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d4a2-143">Header</span><span class="sxs-lookup"><span data-stu-id="6d4a2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d4a2-144"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d4a2-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4a2-145">См. также</span><span class="sxs-lookup"><span data-stu-id="6d4a2-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d4a2-146">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="6d4a2-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d4a2-147">**EM \_**</span><span class="sxs-lookup"><span data-stu-id="6d4a2-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="6d4a2-148">**EM \_ сетректнп**</span><span class="sxs-lookup"><span data-stu-id="6d4a2-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="6d4a2-149">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="6d4a2-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6d4a2-150">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d4a2-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 


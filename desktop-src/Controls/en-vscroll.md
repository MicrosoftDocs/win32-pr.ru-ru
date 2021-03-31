---
title: Код уведомления EN_VSCROLL (Winuser. h)
description: Посылается, когда пользователь щелкает вертикальную полосу прокрутки элемента управления правки или когда пользователь прокручивает колесико мыши над элементом управления "поле ввода".
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892694"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="c9eaf-104">\_Код уведомления EN VSCROLL</span><span class="sxs-lookup"><span data-stu-id="c9eaf-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="c9eaf-105">Посылается, когда пользователь щелкает вертикальную полосу прокрутки элемента управления правки или когда пользователь прокручивает колесико мыши над элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c9eaf-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="c9eaf-106">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c9eaf-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="c9eaf-107">Родительское окно уведомляется перед обновлением экрана.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c9eaf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9eaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9eaf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9eaf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9eaf-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c9eaf-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="c9eaf-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c9eaf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9eaf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9eaf-113">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c9eaf-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9eaf-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9eaf-114">Remarks</span></span>

<span data-ttu-id="c9eaf-115">Это сообщение отправляется для следующих событий мыши на вертикальной полосе прокрутки: нажатием кнопки со стрелкой или нажатием кнопки со стрелкой и бегунком.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="c9eaf-116">Однако при щелчке мышью на панели прокрутки сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="c9eaf-117">Сообщение также отправляется, когда событие клавиатуры вызывает изменение в области просмотра элемента управления "поле ввода", например, при нажатии клавиш домой, конец, страница вверх, страница вниз, стрелка вверх или стрелка вниз.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="c9eaf-118">Колесико мыши — это мышь с центральным колесиком, которое прокручивается.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="c9eaf-119">Дополнительные сведения см. в разделе "колесико мыши" раздела [о вводе](/windows/desktop/inputdev/about-mouse-input)с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="c9eaf-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c9eaf-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c9eaf-121">Чтобы получить \_ коды уведомлений EN VSCROLL, укажите [**енм \_ прокрутку**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="c9eaf-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="c9eaf-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c9eaf-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9eaf-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c9eaf-123">Requirements</span></span>



| <span data-ttu-id="c9eaf-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c9eaf-124">Requirement</span></span> | <span data-ttu-id="c9eaf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c9eaf-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eaf-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9eaf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9eaf-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9eaf-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9eaf-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9eaf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9eaf-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9eaf-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9eaf-130">Header</span><span class="sxs-lookup"><span data-stu-id="c9eaf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9eaf-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9eaf-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9eaf-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9eaf-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9eaf-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c9eaf-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c9eaf-134">EN \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="c9eaf-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="c9eaf-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c9eaf-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9eaf-136">Использование элементов управления Edit</span><span class="sxs-lookup"><span data-stu-id="c9eaf-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="c9eaf-137">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c9eaf-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c9eaf-138">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="c9eaf-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


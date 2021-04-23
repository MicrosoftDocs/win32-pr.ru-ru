---
title: Код уведомления EN_HSCROLL (Winuser. h)
description: Посылается, когда пользователь щелкает горизонтальную полосу прокрутки элемента управления Edit. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM. Родительское окно уведомляется перед обновлением экрана.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892150"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="8af67-106">\_Код уведомления EN HSCROLL</span><span class="sxs-lookup"><span data-stu-id="8af67-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="8af67-107">Посылается, когда пользователь щелкает горизонтальную полосу прокрутки элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="8af67-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="8af67-108">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8af67-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="8af67-109">Родительское окно уведомляется перед обновлением экрана.</span><span class="sxs-lookup"><span data-stu-id="8af67-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="8af67-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8af67-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af67-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8af67-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af67-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="8af67-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="8af67-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="8af67-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8af67-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8af67-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af67-115">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="8af67-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8af67-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8af67-116">Remarks</span></span>

<span data-ttu-id="8af67-117">Этот код уведомления отправляется для следующих событий мыши на горизонтальной полосе прокрутки: нажатием кнопки со стрелкой или нажатием кнопки со стрелкой и бегунком.</span><span class="sxs-lookup"><span data-stu-id="8af67-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="8af67-118">Однако код уведомления не отправляется при щелчке самого бегунка полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8af67-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="8af67-119">Код уведомления также отправляется, когда событие клавиатуры вызывает изменение в области просмотра элемента управления "поле ввода", например, с помощью клавиш HOME, конец, стрелка влево или стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="8af67-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="8af67-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8af67-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8af67-121">Чтобы получить коды уведомлений **en \_ HSCROLL** , укажите [**енм \_ прокрутку**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="8af67-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="8af67-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8af67-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8af67-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8af67-123">Requirements</span></span>



| <span data-ttu-id="8af67-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8af67-124">Requirement</span></span> | <span data-ttu-id="8af67-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8af67-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af67-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8af67-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8af67-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8af67-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8af67-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8af67-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8af67-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8af67-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8af67-130">Header</span><span class="sxs-lookup"><span data-stu-id="8af67-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af67-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8af67-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af67-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8af67-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="8af67-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8af67-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8af67-134">EN \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="8af67-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="8af67-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="8af67-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8af67-136">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="8af67-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


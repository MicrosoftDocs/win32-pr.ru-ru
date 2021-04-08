---
title: Код уведомления DTN_DROPDOWN (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь активирует раскрывающийся календарь с раскрывающимся списком. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892289"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="9a294-105">\_Код уведомления раскрывающегося списка ДТН</span><span class="sxs-lookup"><span data-stu-id="9a294-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="9a294-106">Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь активирует раскрывающийся календарь с раскрывающимся списком.</span><span class="sxs-lookup"><span data-stu-id="9a294-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="9a294-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9a294-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="9a294-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a294-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a294-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a294-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a294-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения об уведомлении.</span><span class="sxs-lookup"><span data-stu-id="9a294-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a294-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a294-111">Return value</span></span>

<span data-ttu-id="9a294-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="9a294-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a294-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a294-113">Remarks</span></span>

<span data-ttu-id="9a294-114">Одной из задач, которые может потребоваться обработчику уведомлений, является настройка элемента управления "месячный месяц — календарь".</span><span class="sxs-lookup"><span data-stu-id="9a294-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="9a294-115">Например, если вы не хотите "переходить на сегодня", необходимо задать стиль [**MCS \_ Today**](month-calendar-control-styles.md)  для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9a294-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="9a294-116">Чтобы получить маркер элемента управления "месячный календарь", отправьте DTP элемент управления [**DTM \_ жетмонскал**](dtm-getmonthcal.md) Message.</span><span class="sxs-lookup"><span data-stu-id="9a294-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="9a294-117">Затем можно использовать этот маркер и [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , чтобы установить нужный стиль "месяц-календарь".</span><span class="sxs-lookup"><span data-stu-id="9a294-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="9a294-118">Элементы управления DTP не поддерживают статический элемент управления Calendar в виде вложенного месяца.</span><span class="sxs-lookup"><span data-stu-id="9a294-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="9a294-119">Элемент управления DTP создает новый элемент управления "месячный календарь" перед отправкой этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="9a294-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="9a294-120">Кроме того, элемент управления DTP уничтожает дочерний элемент управления, когда он неактивен (видимый).</span><span class="sxs-lookup"><span data-stu-id="9a294-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="9a294-121">Поэтому приложение не должно полагаться на статический обработчик окна для дочернего месяца элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9a294-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a294-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9a294-122">Requirements</span></span>



| <span data-ttu-id="9a294-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9a294-123">Requirement</span></span> | <span data-ttu-id="9a294-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9a294-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a294-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a294-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a294-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a294-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a294-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a294-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a294-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a294-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a294-129">Header</span><span class="sxs-lookup"><span data-stu-id="9a294-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a294-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a294-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a294-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a294-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a294-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9a294-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a294-133">ДТН \_ крупный план</span><span class="sxs-lookup"><span data-stu-id="9a294-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="9a294-134">**DTM \_ жетмонскал**</span><span class="sxs-lookup"><span data-stu-id="9a294-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 


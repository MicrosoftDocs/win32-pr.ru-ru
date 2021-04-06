---
title: Код уведомления DTN_CLOSEUP (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь закрывает календарь раскрывающегося списка.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803274"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="1785d-104">\_Код уведомления ДТН крупный план</span><span class="sxs-lookup"><span data-stu-id="1785d-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="1785d-105">Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь закрывает календарь раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="1785d-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="1785d-106">Месячный календарь закрывается, когда пользователь выбирает дату из календаря месяца или щелкает стрелку раскрывающегося списка, когда календарь открыт.</span><span class="sxs-lookup"><span data-stu-id="1785d-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="1785d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1785d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="1785d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1785d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1785d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1785d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1785d-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения об уведомлении.</span><span class="sxs-lookup"><span data-stu-id="1785d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1785d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1785d-111">Return value</span></span>

<span data-ttu-id="1785d-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="1785d-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1785d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1785d-113">Remarks</span></span>

<span data-ttu-id="1785d-114">Элементы управления DTP не поддерживают статический элемент управления Calendar в виде вложенного месяца.</span><span class="sxs-lookup"><span data-stu-id="1785d-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="1785d-115">Элемент управления DTP уничтожает элемент управления Calendar в дочернем месяце перед отправкой этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="1785d-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="1785d-116">Поэтому приложение не должно полагаться на статический обработчик окна для дочернего месяца элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1785d-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="1785d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1785d-117">Requirements</span></span>



| <span data-ttu-id="1785d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1785d-118">Requirement</span></span> | <span data-ttu-id="1785d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1785d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1785d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1785d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1785d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1785d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1785d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1785d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1785d-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1785d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1785d-124">Header</span><span class="sxs-lookup"><span data-stu-id="1785d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1785d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1785d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1785d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1785d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1785d-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1785d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1785d-128">\_раскрывающийся список ДТН</span><span class="sxs-lookup"><span data-stu-id="1785d-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="1785d-129">**DTM \_ жетмонскал**</span><span class="sxs-lookup"><span data-stu-id="1785d-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 






---
title: Код уведомления EN_SETFOCUS (Winuser. h)
description: Посылается, когда элемент управления "поле ввода" получает фокус клавиатуры. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- EN_SETFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803425"
---
# <a name="en_setfocus-notification-code"></a><span data-ttu-id="bdc5c-105">\_Код уведомления "EN SETFOCUS"</span><span class="sxs-lookup"><span data-stu-id="bdc5c-105">EN\_SETFOCUS notification code</span></span>

<span data-ttu-id="bdc5c-106">Посылается, когда элемент управления "поле ввода" получает фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="bdc5c-106">Sent when an edit control receives the keyboard focus.</span></span> <span data-ttu-id="bdc5c-107">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="bdc5c-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="bdc5c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdc5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc5c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc5c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc5c-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="bdc5c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="bdc5c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="bdc5c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="bdc5c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc5c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc5c-113">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="bdc5c-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdc5c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdc5c-114">Remarks</span></span>

<span data-ttu-id="bdc5c-115">Родительское окно всегда получает [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="bdc5c-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="bdc5c-116">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bdc5c-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bdc5c-117">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="bdc5c-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc5c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bdc5c-118">Requirements</span></span>



| <span data-ttu-id="bdc5c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bdc5c-119">Requirement</span></span> | <span data-ttu-id="bdc5c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bdc5c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc5c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdc5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc5c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdc5c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdc5c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdc5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc5c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdc5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdc5c-125">Header</span><span class="sxs-lookup"><span data-stu-id="bdc5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc5c-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdc5c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc5c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdc5c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdc5c-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="bdc5c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdc5c-129">EN \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="bdc5c-129">EN\_KILLFOCUS</span></span>](en-killfocus.md)
</dt> <dt>

<span data-ttu-id="bdc5c-130">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="bdc5c-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bdc5c-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="bdc5c-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


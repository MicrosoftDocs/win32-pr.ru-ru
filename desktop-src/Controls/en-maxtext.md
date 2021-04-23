---
title: Код уведомления EN_MAXTEXT (Winuser. h)
description: Посылается, когда текущая Вставка текста превысила указанное количество символов для элемента управления "поле ввода".
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535045"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="719ba-104">\_Код уведомления EN макстекст</span><span class="sxs-lookup"><span data-stu-id="719ba-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="719ba-105">Посылается, когда текущая Вставка текста превысила указанное количество символов для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="719ba-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="719ba-106">Вставка текста была усечена.</span><span class="sxs-lookup"><span data-stu-id="719ba-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="719ba-107">Этот код уведомления также отправляется, если в элементе управления "поле ввода" нет стиля [**\_ аутохскролл**](edit-control-styles.md) , а число вставляемых символов превысит ширину элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="719ba-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="719ba-108">Этот код уведомления также отправляется, когда элемент управления "поле ввода" не имеет стиля [**\_ аутовскролл**](edit-control-styles.md) , а общее число строк, полученное при вставке текста, превысит высоту элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="719ba-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="719ba-109">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="719ba-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="719ba-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="719ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719ba-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="719ba-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="719ba-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="719ba-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="719ba-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="719ba-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="719ba-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="719ba-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="719ba-115">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="719ba-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="719ba-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="719ba-116">Remarks</span></span>

<span data-ttu-id="719ba-117">Родительское окно всегда получает [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="719ba-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="719ba-118">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="719ba-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="719ba-119">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="719ba-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="719ba-120">Требования</span><span class="sxs-lookup"><span data-stu-id="719ba-120">Requirements</span></span>



| <span data-ttu-id="719ba-121">Требование</span><span class="sxs-lookup"><span data-stu-id="719ba-121">Requirement</span></span> | <span data-ttu-id="719ba-122">Значение</span><span class="sxs-lookup"><span data-stu-id="719ba-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="719ba-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="719ba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="719ba-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="719ba-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="719ba-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="719ba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="719ba-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="719ba-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="719ba-127">Header</span><span class="sxs-lookup"><span data-stu-id="719ba-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="719ba-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="719ba-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="719ba-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="719ba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719ba-130">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="719ba-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


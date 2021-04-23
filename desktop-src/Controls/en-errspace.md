---
title: Код уведомления EN_ERRSPACE (Winuser. h)
description: Посылается, когда элемент управления "изменение" не может выделить достаточно памяти для удовлетворения определенного запроса. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891510"
---
# <a name="en_errspace-notification-code"></a><span data-ttu-id="6d958-105">\_Код уведомления EN еррспаце</span><span class="sxs-lookup"><span data-stu-id="6d958-105">EN\_ERRSPACE notification code</span></span>

<span data-ttu-id="6d958-106">Посылается, когда элемент управления "изменение" не может выделить достаточно памяти для удовлетворения определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="6d958-106">Sent when an edit control cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="6d958-107">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6d958-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d958-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d958-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d958-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d958-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6d958-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="6d958-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="6d958-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6d958-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d958-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d958-113">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6d958-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d958-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d958-114">Remarks</span></span>

<span data-ttu-id="6d958-115">Родительское окно всегда будет получать [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) для этого события. для него не требуется отправка маски уведомления с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="6d958-115">The parent window will always get a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event; it does not require a notification mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="6d958-116">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="6d958-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6d958-117">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6d958-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d958-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6d958-118">Requirements</span></span>



| <span data-ttu-id="6d958-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6d958-119">Requirement</span></span> | <span data-ttu-id="6d958-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6d958-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d958-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d958-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d958-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d958-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d958-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d958-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d958-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d958-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d958-125">Header</span><span class="sxs-lookup"><span data-stu-id="6d958-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d958-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d958-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d958-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d958-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d958-128">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="6d958-128">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


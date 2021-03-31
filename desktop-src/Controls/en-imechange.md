---
title: Код уведомления EN_IMECHANGE (RichEdit. h)
description: Сообщает родителю элемента управления Rich Edit, что изменилось состояние преобразования редактора IME.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071657"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="3604f-104">\_Код уведомления EN имечанже</span><span class="sxs-lookup"><span data-stu-id="3604f-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="3604f-105">Сообщает родителю элемента управления Rich Edit, что изменилось состояние преобразования редактора IME.</span><span class="sxs-lookup"><span data-stu-id="3604f-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="3604f-106">Этот код уведомления доступен *только* для азиатских языковых версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3604f-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="3604f-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в [**виде \_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="3604f-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3604f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3604f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3604f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3604f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3604f-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3604f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="3604f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="3604f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="3604f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3604f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3604f-113">Обработчик для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3604f-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3604f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3604f-114">Return value</span></span>

<span data-ttu-id="3604f-115">Этот код уведомления возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3604f-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3604f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3604f-116">Remarks</span></span>

<span data-ttu-id="3604f-117">Чтобы получить \_ коды уведомлений EN имечанже, укажите [**енм \_ имечанже**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="3604f-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="3604f-118">Этот код уведомления поддерживается только в азиатской версии Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="3604f-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="3604f-119">Он не поддерживается в более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3604f-119">It is not supported in later versions.</span></span> <span data-ttu-id="3604f-120">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="3604f-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3604f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3604f-121">Requirements</span></span>



| <span data-ttu-id="3604f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3604f-122">Requirement</span></span> | <span data-ttu-id="3604f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3604f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3604f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3604f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3604f-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3604f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3604f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3604f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3604f-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3604f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3604f-128">Header</span><span class="sxs-lookup"><span data-stu-id="3604f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3604f-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3604f-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3604f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3604f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3604f-131">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3604f-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="3604f-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3604f-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3604f-133">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3604f-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3604f-134">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="3604f-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


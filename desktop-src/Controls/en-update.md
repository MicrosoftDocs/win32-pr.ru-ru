---
title: Код уведомления EN_UPDATE (Winuser. h)
description: Посылается, когда элемент управления "изменение" собирается перерисовывать себя.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137146"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="f17c4-104">\_Код уведомления об обновлении EN</span><span class="sxs-lookup"><span data-stu-id="f17c4-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="f17c4-105">Посылается, когда элемент управления "изменение" собирается перерисовывать себя.</span><span class="sxs-lookup"><span data-stu-id="f17c4-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="f17c4-106">Этот код уведомления отправляется после того, как элемент управления отформатирует текст, но перед отображением текста.</span><span class="sxs-lookup"><span data-stu-id="f17c4-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="f17c4-107">Это позволяет изменить размер окна элемента управления редактированием, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f17c4-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="f17c4-108">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f17c4-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f17c4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f17c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17c4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f17c4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f17c4-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="f17c4-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="f17c4-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f17c4-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f17c4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f17c4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f17c4-114">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="f17c4-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f17c4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f17c4-115">Remarks</span></span>

<span data-ttu-id="f17c4-116">**Расширенное редактирование 1,0:** Чтобы получить \_ коды уведомлений о коротком обновлении, укажите [**\_ Обновление енм**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f17c4-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="f17c4-117">**Расширенное редактирование 2,0 и более поздних версий:** Флаг [**\_ обновления енм**](rich-edit-control-event-mask-flags.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f17c4-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="f17c4-118">\_Всегда получается код уведомления о коротком обновлении.</span><span class="sxs-lookup"><span data-stu-id="f17c4-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="f17c4-119">Тем не менее, когда Microsoft Rich Editing 3,0 эмулирует Microsoft Rich Edit 1,0, чтобы получить \_ коды уведомлений для обновления EN, необходимо указать **енм \_ Обновление** в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f17c4-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="f17c4-120">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f17c4-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f17c4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f17c4-121">Requirements</span></span>



| <span data-ttu-id="f17c4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f17c4-122">Requirement</span></span> | <span data-ttu-id="f17c4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f17c4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f17c4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f17c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f17c4-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f17c4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f17c4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f17c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f17c4-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f17c4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f17c4-128">Header</span><span class="sxs-lookup"><span data-stu-id="f17c4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f17c4-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f17c4-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f17c4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f17c4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f17c4-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f17c4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f17c4-132">\_изменение EN</span><span class="sxs-lookup"><span data-stu-id="f17c4-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="f17c4-133">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="f17c4-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f17c4-134">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="f17c4-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


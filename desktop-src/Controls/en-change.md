---
title: Код уведомления EN_CHANGE (Winuser. h)
description: Посылается, когда пользователь затратил действие, которое может изменить текст в элементе управления "поле ввода".
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891709"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="0f29c-104">\_Код уведомления об изменении EN</span><span class="sxs-lookup"><span data-stu-id="0f29c-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="0f29c-105">Посылается, когда пользователь затратил действие, которое может изменить текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="0f29c-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="0f29c-106">В отличие от кода уведомления о [ \_ обновлении](en-update.md) , этот код уведомления отправляется после того, как система обновляет экран.</span><span class="sxs-lookup"><span data-stu-id="0f29c-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="0f29c-107">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0f29c-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0f29c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f29c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f29c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f29c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f29c-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="0f29c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="0f29c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="0f29c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0f29c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f29c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f29c-113">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="0f29c-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f29c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f29c-114">Remarks</span></span>

<span data-ttu-id="0f29c-115">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="0f29c-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="0f29c-116">Чтобы получить \_ коды уведомлений о смене, укажите [**енм \_ изменения**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="0f29c-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="0f29c-117">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0f29c-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="0f29c-118">\_Код уведомления о смене на короткое время не отправляется, если используется [**\_ Многострочный стиль ES**](edit-control-styles.md) и текст отправляется через [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="0f29c-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f29c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0f29c-119">Requirements</span></span>



| <span data-ttu-id="0f29c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0f29c-120">Requirement</span></span> | <span data-ttu-id="0f29c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0f29c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f29c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f29c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f29c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f29c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0f29c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f29c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f29c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f29c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f29c-126">Header</span><span class="sxs-lookup"><span data-stu-id="0f29c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f29c-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f29c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f29c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f29c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f29c-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0f29c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f29c-130">\_Обновление EN</span><span class="sxs-lookup"><span data-stu-id="0f29c-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="0f29c-131">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="0f29c-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0f29c-132">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="0f29c-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


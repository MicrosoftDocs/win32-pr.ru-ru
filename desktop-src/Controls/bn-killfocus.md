---
title: Код уведомления BN_KILLFOCUS (Winuser. h)
description: Посылается, когда кнопка теряет фокус клавиатуры. \_Для отправки этого кода уведомления кнопка должна иметь стиль уведомления "BS". Родительское окно кнопки получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489645"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="e2b90-106">\_Код уведомления млрд долл киллфокус</span><span class="sxs-lookup"><span data-stu-id="e2b90-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="e2b90-107">Посылается, когда кнопка теряет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="e2b90-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="e2b90-108">Для отправки этого кода уведомления кнопка должна иметь стиль [**\_ уведомления "BS**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="e2b90-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="e2b90-109">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e2b90-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e2b90-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2b90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b90-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2b90-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b90-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="e2b90-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="e2b90-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="e2b90-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e2b90-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2b90-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b90-115">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="e2b90-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b90-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e2b90-116">Requirements</span></span>



| <span data-ttu-id="e2b90-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e2b90-117">Requirement</span></span> | <span data-ttu-id="e2b90-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b90-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b90-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2b90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b90-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2b90-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2b90-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2b90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b90-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2b90-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2b90-123">Header</span><span class="sxs-lookup"><span data-stu-id="e2b90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b90-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2b90-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b90-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2b90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b90-126">МЛРД долл \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="e2b90-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 


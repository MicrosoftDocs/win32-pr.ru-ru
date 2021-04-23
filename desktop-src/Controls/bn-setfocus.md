---
title: Код уведомления BN_SETFOCUS (Winuser. h)
description: Посылается, когда кнопка получает фокус клавиатуры. \_Для отправки этого кода уведомления кнопка должна иметь стиль уведомления "BS". Родительское окно кнопки получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654446"
---
# <a name="bn_setfocus-notification-code"></a><span data-ttu-id="b2477-106">\_Код уведомления млрд долл SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="b2477-106">BN\_SETFOCUS notification code</span></span>

<span data-ttu-id="b2477-107">Посылается, когда кнопка получает фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b2477-107">Sent when a button receives the keyboard focus.</span></span> <span data-ttu-id="b2477-108">Для отправки этого кода уведомления кнопка должна иметь стиль [**\_ уведомления "BS**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="b2477-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="b2477-109">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b2477-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b2477-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2477-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2477-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2477-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2477-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="b2477-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="b2477-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="b2477-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b2477-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2477-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2477-115">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="b2477-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2477-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b2477-116">Requirements</span></span>



| <span data-ttu-id="b2477-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b2477-117">Requirement</span></span> | <span data-ttu-id="b2477-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b2477-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2477-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2477-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2477-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2477-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2477-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2477-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2477-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2477-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2477-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2477-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2477-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2477-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2477-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2477-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2477-126">МЛРД долл \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="b2477-126">BN\_KILLFOCUS</span></span>](bn-killfocus.md)
</dt> </dl>

 


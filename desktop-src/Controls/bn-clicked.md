---
title: Код уведомления BN_CLICKED (Winuser. h)
description: Посылается, когда пользователь нажимает кнопку. Родительское окно кнопки получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- BN_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135467"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="3db10-105">МЛРД долл \_ щелчок по коду уведомления</span><span class="sxs-lookup"><span data-stu-id="3db10-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="3db10-106">Посылается, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="3db10-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="3db10-107">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="3db10-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="3db10-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3db10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db10-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3db10-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3db10-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="3db10-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="3db10-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="3db10-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="3db10-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3db10-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3db10-113">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="3db10-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3db10-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3db10-114">Remarks</span></span>

<span data-ttu-id="3db10-115">Отключенная кнопка не отправляет млрд долл \_ щелчком по коду уведомления в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="3db10-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db10-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3db10-116">Requirements</span></span>



| <span data-ttu-id="3db10-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3db10-117">Requirement</span></span> | <span data-ttu-id="3db10-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3db10-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db10-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3db10-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3db10-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3db10-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3db10-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3db10-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3db10-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3db10-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3db10-123">Header</span><span class="sxs-lookup"><span data-stu-id="3db10-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db10-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3db10-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db10-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3db10-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3db10-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3db10-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="3db10-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3db10-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3db10-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3db10-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3db10-129">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="3db10-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


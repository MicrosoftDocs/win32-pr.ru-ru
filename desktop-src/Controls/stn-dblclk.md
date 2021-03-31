---
title: Код уведомления STN_DBLCLK (Winuser. h)
description: '\_Код уведомления СТН дблклк отправляется, когда пользователь дважды щелкает статический элемент управления, который имеет \_ стиль SS notify. Родительское окно элемента управления получает этот код уведомления через \_ командное сообщение WM.'
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071325"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="4be8a-105">\_Код уведомления СТН дблклк</span><span class="sxs-lookup"><span data-stu-id="4be8a-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="4be8a-106">\_Код уведомления СТН дблклк отправляется, когда пользователь дважды щелкает статический элемент управления, который имеет стиль [**SS \_ Notify**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4be8a-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="4be8a-107">Родительское окно элемента управления получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="4be8a-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4be8a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4be8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be8a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4be8a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be8a-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4be8a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="4be8a-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="4be8a-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4be8a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4be8a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be8a-113">Обработчик статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4be8a-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4be8a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4be8a-114">Requirements</span></span>



| <span data-ttu-id="4be8a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4be8a-115">Requirement</span></span> | <span data-ttu-id="4be8a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4be8a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be8a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4be8a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4be8a-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4be8a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4be8a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4be8a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4be8a-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4be8a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4be8a-121">Header</span><span class="sxs-lookup"><span data-stu-id="4be8a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be8a-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4be8a-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be8a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4be8a-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="4be8a-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4be8a-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4be8a-125">\_щелчок СТН</span><span class="sxs-lookup"><span data-stu-id="4be8a-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="4be8a-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4be8a-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4be8a-127">Статические элементы управления</span><span class="sxs-lookup"><span data-stu-id="4be8a-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="4be8a-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="4be8a-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4be8a-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4be8a-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="4be8a-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4be8a-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4be8a-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="4be8a-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


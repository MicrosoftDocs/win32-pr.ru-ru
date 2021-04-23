---
title: Код уведомления CBN_KILLFOCUS (Winuser. h)
description: Посылается, когда поле со списком теряет фокус клавиатуры. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 0118a2ff-9811-4bf1-b3f6-1d00ca5c8dbe
keywords:
- CBN_KILLFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e266824bf8bcdac1fb901d40ca2b15406fc79660
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654705"
---
# <a name="cbn_killfocus-notification-code"></a><span data-ttu-id="a74cb-105">\_Код уведомления КБН киллфокус</span><span class="sxs-lookup"><span data-stu-id="a74cb-105">CBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="a74cb-106">Посылается, когда поле со списком теряет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a74cb-106">Sent when a combo box loses the keyboard focus.</span></span> <span data-ttu-id="a74cb-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a74cb-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a74cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a74cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a74cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74cb-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="a74cb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="a74cb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="a74cb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a74cb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a74cb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74cb-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="a74cb-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a74cb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a74cb-114">Requirements</span></span>



| <span data-ttu-id="a74cb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a74cb-115">Requirement</span></span> | <span data-ttu-id="a74cb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a74cb-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a74cb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a74cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a74cb-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a74cb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a74cb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a74cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a74cb-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a74cb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a74cb-121">Header</span><span class="sxs-lookup"><span data-stu-id="a74cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74cb-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a74cb-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74cb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a74cb-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a74cb-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a74cb-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a74cb-125">КБН \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="a74cb-125">CBN\_SETFOCUS</span></span>](cbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="a74cb-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="a74cb-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a74cb-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a74cb-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a74cb-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a74cb-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a74cb-129">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="a74cb-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


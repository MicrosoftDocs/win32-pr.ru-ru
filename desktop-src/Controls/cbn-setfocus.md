---
title: Код уведомления CBN_SETFOCUS (Winuser. h)
description: Посылается, когда поле со списком получает фокус клавиатуры. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- CBN_SETFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341380"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="5c7bc-105">\_Код уведомления КБН SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="5c7bc-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="5c7bc-106">Посылается, когда поле со списком получает фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="5c7bc-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5c7bc-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5c7bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c7bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c7bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7bc-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="5c7bc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5c7bc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c7bc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7bc-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c7bc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5c7bc-114">Requirements</span></span>



| <span data-ttu-id="5c7bc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5c7bc-115">Requirement</span></span> | <span data-ttu-id="5c7bc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7bc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7bc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c7bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7bc-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c7bc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c7bc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c7bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7bc-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c7bc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c7bc-121">Header</span><span class="sxs-lookup"><span data-stu-id="5c7bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7bc-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c7bc-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7bc-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c7bc-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c7bc-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c7bc-125">КБН \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="5c7bc-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="5c7bc-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5c7bc-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c7bc-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5c7bc-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c7bc-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5c7bc-129">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


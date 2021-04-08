---
title: Код уведомления LBN_SETFOCUS (Winuser. h)
description: Уведомляет приложение о том, что в списке получен фокус клавиатуры. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- LBN_SETFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891962"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="06f36-105">\_Код уведомления ЛБН SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="06f36-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="06f36-106">Уведомляет приложение о том, что в списке получен фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="06f36-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="06f36-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="06f36-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="06f36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="06f36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f36-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06f36-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06f36-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="06f36-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="06f36-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="06f36-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="06f36-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06f36-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06f36-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="06f36-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06f36-114">Требования</span><span class="sxs-lookup"><span data-stu-id="06f36-114">Requirements</span></span>



| <span data-ttu-id="06f36-115">Требование</span><span class="sxs-lookup"><span data-stu-id="06f36-115">Requirement</span></span> | <span data-ttu-id="06f36-116">Значение</span><span class="sxs-lookup"><span data-stu-id="06f36-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f36-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06f36-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06f36-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06f36-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="06f36-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06f36-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06f36-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06f36-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06f36-121">Header</span><span class="sxs-lookup"><span data-stu-id="06f36-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06f36-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06f36-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f36-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06f36-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="06f36-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="06f36-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06f36-125">ЛБН \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="06f36-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="06f36-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="06f36-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="06f36-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06f36-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="06f36-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06f36-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06f36-129">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="06f36-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


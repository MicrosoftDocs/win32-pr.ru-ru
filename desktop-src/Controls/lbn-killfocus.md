---
title: Код уведомления LBN_KILLFOCUS (Winuser. h)
description: Уведомляет приложение о том, что список потерял фокус клавиатуры. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- LBN_KILLFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba424efc2518d359c3d031561aeafee8c0348b65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137123"
---
# <a name="lbn_killfocus-notification-code"></a><span data-ttu-id="41108-105">\_Код уведомления ЛБН киллфокус</span><span class="sxs-lookup"><span data-stu-id="41108-105">LBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="41108-106">Уведомляет приложение о том, что список потерял фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="41108-106">Notifies the application that the list box has lost the keyboard focus.</span></span> <span data-ttu-id="41108-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="41108-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="41108-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41108-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41108-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41108-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="41108-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="41108-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="41108-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="41108-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41108-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41108-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="41108-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41108-114">Требования</span><span class="sxs-lookup"><span data-stu-id="41108-114">Requirements</span></span>



| <span data-ttu-id="41108-115">Требование</span><span class="sxs-lookup"><span data-stu-id="41108-115">Requirement</span></span> | <span data-ttu-id="41108-116">Значение</span><span class="sxs-lookup"><span data-stu-id="41108-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41108-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41108-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41108-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41108-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41108-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41108-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41108-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41108-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41108-121">Header</span><span class="sxs-lookup"><span data-stu-id="41108-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41108-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41108-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41108-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41108-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="41108-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="41108-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="41108-125">ЛБН \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="41108-125">LBN\_SETFOCUS</span></span>](lbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="41108-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="41108-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="41108-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41108-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="41108-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41108-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="41108-129">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="41108-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


---
title: Код уведомления CBN_ERRSPACE (Winuser. h)
description: Посылается, если поле со списком не может выделить достаточно памяти для удовлетворения конкретного запроса. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- CBN_ERRSPACE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137634"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="84150-105">\_Код уведомления КБН еррспаце</span><span class="sxs-lookup"><span data-stu-id="84150-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="84150-106">Посылается, если поле со списком не может выделить достаточно памяти для удовлетворения конкретного запроса.</span><span class="sxs-lookup"><span data-stu-id="84150-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="84150-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="84150-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="84150-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84150-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84150-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84150-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="84150-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="84150-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="84150-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="84150-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84150-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84150-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="84150-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84150-114">Требования</span><span class="sxs-lookup"><span data-stu-id="84150-114">Requirements</span></span>



| <span data-ttu-id="84150-115">Требование</span><span class="sxs-lookup"><span data-stu-id="84150-115">Requirement</span></span> | <span data-ttu-id="84150-116">Значение</span><span class="sxs-lookup"><span data-stu-id="84150-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84150-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84150-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84150-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84150-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84150-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84150-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84150-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84150-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84150-121">Header</span><span class="sxs-lookup"><span data-stu-id="84150-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="84150-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84150-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84150-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84150-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="84150-124">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="84150-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="84150-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84150-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="84150-126">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84150-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84150-127">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="84150-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


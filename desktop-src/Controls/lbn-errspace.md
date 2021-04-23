---
title: Код уведомления LBN_ERRSPACE (Winuser. h)
description: Уведомляет приложение о том, что список не может выделить достаточно памяти для удовлетворения конкретного запроса. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262210"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="f7f56-105">\_Код уведомления ЛБН еррспаце</span><span class="sxs-lookup"><span data-stu-id="f7f56-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="f7f56-106">Уведомляет приложение о том, что список не может выделить достаточно памяти для удовлетворения конкретного запроса.</span><span class="sxs-lookup"><span data-stu-id="f7f56-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="f7f56-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f7f56-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f7f56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7f56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f56-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7f56-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f56-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="f7f56-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="f7f56-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f7f56-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f7f56-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7f56-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f56-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="f7f56-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7f56-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f7f56-114">Requirements</span></span>



| <span data-ttu-id="f7f56-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f7f56-115">Requirement</span></span> | <span data-ttu-id="f7f56-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f7f56-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f56-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7f56-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f56-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7f56-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f7f56-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7f56-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f56-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7f56-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7f56-121">Header</span><span class="sxs-lookup"><span data-stu-id="f7f56-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7f56-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7f56-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f56-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7f56-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7f56-124">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="f7f56-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f7f56-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7f56-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f7f56-126">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7f56-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f7f56-127">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="f7f56-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


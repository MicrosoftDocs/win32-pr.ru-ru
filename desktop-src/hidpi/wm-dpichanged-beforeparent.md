---
title: Сообщение WM_DPICHANGED_BEFOREPARENT (Winuser. h)
description: Для окон верхнего уровня на мониторе версии 2 это сообщение отправляется во все HWND в дочернем дереве ХВДН окна, которое является изменением DPI. | Сообщение WM_DPICHANGED_BEFOREPARENT (Winuser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT высокое разрешение для сообщения
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000264"
---
# <a name="wm_dpichanged_beforeparent-message"></a><span data-ttu-id="69b68-105">\_Сообщение WM DPICHANGED \_ бефорепарент</span><span class="sxs-lookup"><span data-stu-id="69b68-105">WM\_DPICHANGED\_BEFOREPARENT message</span></span>

<span data-ttu-id="69b68-106">Для окон верхнего уровня [на мониторе версии 2](dpi-awareness-context.md) это сообщение отправляется во все HWND в дочернем дереве хвдн окна, которое является изменением dpi.</span><span class="sxs-lookup"><span data-stu-id="69b68-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="69b68-107">Это сообщение появляется перед тем, как окно верхнего уровня получает [**WM \_ DPICHANGED**](wm-dpichanged.md)и проходит по дочернему дереву снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="69b68-107">This message occurs before the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the bottom up.</span></span>


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a><span data-ttu-id="69b68-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="69b68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b68-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69b68-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69b68-110">Это значение не используется и будет равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="69b68-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="69b68-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69b68-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69b68-112">Это значение не используется и будет равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="69b68-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b68-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69b68-113">Return value</span></span>

<span data-ttu-id="69b68-114">Это значение не используется и игнорируется системой.</span><span class="sxs-lookup"><span data-stu-id="69b68-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b68-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69b68-115">Remarks</span></span>

<span data-ttu-id="69b68-116">Обработка этого сообщения по умолчанию в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)отсутствует.</span><span class="sxs-lookup"><span data-stu-id="69b68-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="69b68-117">Это сообщение отправляется только в том случае, если окно верхнего уровня имеет контекст с отслеживанием DPI для PMv2.</span><span class="sxs-lookup"><span data-stu-id="69b68-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b68-118">Требования</span><span class="sxs-lookup"><span data-stu-id="69b68-118">Requirements</span></span>



| <span data-ttu-id="69b68-119">Требование</span><span class="sxs-lookup"><span data-stu-id="69b68-119">Requirement</span></span> | <span data-ttu-id="69b68-120">Значение</span><span class="sxs-lookup"><span data-stu-id="69b68-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="69b68-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69b68-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69b68-122">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="69b68-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="69b68-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69b68-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69b68-124">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="69b68-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="69b68-125">Header</span><span class="sxs-lookup"><span data-stu-id="69b68-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b68-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b68-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b68-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69b68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b68-128">**WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="69b68-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="69b68-129">**WM \_ DPICHANGED \_ афтерпарент**</span><span class="sxs-lookup"><span data-stu-id="69b68-129">**WM\_DPICHANGED\_AFTERPARENT**</span></span>](wm-dpichanged-afterparent.md)
</dt> </dl>

 


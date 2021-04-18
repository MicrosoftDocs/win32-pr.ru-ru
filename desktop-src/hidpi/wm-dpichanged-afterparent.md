---
title: Сообщение WM_DPICHANGED_AFTERPARENT (Winuser. h)
description: Для окон верхнего уровня на мониторе версии 2 это сообщение отправляется во все HWND в дочернем дереве ХВДН окна, которое является изменением DPI. | Сообщение WM_DPICHANGED_AFTERPARENT (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT высокое разрешение для сообщения
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684960"
---
# <a name="wm_dpichanged_afterparent-message"></a><span data-ttu-id="c81b5-105">\_Сообщение WM DPICHANGED \_ афтерпарент</span><span class="sxs-lookup"><span data-stu-id="c81b5-105">WM\_DPICHANGED\_AFTERPARENT message</span></span>

<span data-ttu-id="c81b5-106">Для окон верхнего уровня [на мониторе версии 2](dpi-awareness-context.md) это сообщение отправляется во все HWND в дочернем дереве хвдн окна, которое является изменением dpi.</span><span class="sxs-lookup"><span data-stu-id="c81b5-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="c81b5-107">Это сообщение появляется после того, как окно верхнего уровня получает [**WM \_ DPICHANGED**](wm-dpichanged.md)и перебирает дочернее дерево сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="c81b5-107">This message occurs after the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the top down.</span></span>


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a><span data-ttu-id="c81b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c81b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c81b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c81b5-110">Это значение не используется и будет равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c81b5-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c81b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c81b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c81b5-112">Это значение не используется и будет равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c81b5-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c81b5-113">Return value</span></span>

<span data-ttu-id="c81b5-114">Это значение не используется и игнорируется системой.</span><span class="sxs-lookup"><span data-stu-id="c81b5-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="c81b5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c81b5-115">Remarks</span></span>

<span data-ttu-id="c81b5-116">Обработка этого сообщения по умолчанию в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c81b5-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="c81b5-117">Это сообщение отправляется только в том случае, если окно верхнего уровня имеет контекст с отслеживанием DPI для PMv2.</span><span class="sxs-lookup"><span data-stu-id="c81b5-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81b5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c81b5-118">Requirements</span></span>



| <span data-ttu-id="c81b5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c81b5-119">Requirement</span></span> | <span data-ttu-id="c81b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c81b5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c81b5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c81b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c81b5-122">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="c81b5-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c81b5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c81b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c81b5-124">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c81b5-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c81b5-125">Header</span><span class="sxs-lookup"><span data-stu-id="c81b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c81b5-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c81b5-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81b5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c81b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81b5-128">**WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="c81b5-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="c81b5-129">**WM \_ DPICHANGED \_ бефорепарент**</span><span class="sxs-lookup"><span data-stu-id="c81b5-129">**WM\_DPICHANGED\_BEFOREPARENT**</span></span>](wm-dpichanged-beforeparent.md)
</dt> </dl>

 


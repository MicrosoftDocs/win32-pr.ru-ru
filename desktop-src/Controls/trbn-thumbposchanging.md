---
title: Код уведомления TRBN_THUMBPOSCHANGING (Коммктрл. h)
description: Уведомляет об изменении расположения бегунка на TrackBar. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000165"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="9c61d-105">\_Код уведомления трбн сумбпосчангинг</span><span class="sxs-lookup"><span data-stu-id="9c61d-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="9c61d-106">Уведомляет об изменении расположения бегунка на TrackBar.</span><span class="sxs-lookup"><span data-stu-id="9c61d-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="9c61d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9c61d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9c61d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c61d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c61d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c61d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c61d-110">Указатель на структуру [**нмтрбсумбпосчангинг**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) .</span><span class="sxs-lookup"><span data-stu-id="9c61d-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="9c61d-111">Вызывающий объект отвечает за выделение этой структуры и задание ее членов, включая элементы содержащейся в ней структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="9c61d-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c61d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c61d-112">Return value</span></span>

<span data-ttu-id="9c61d-113">Возвращает **значение true** , чтобы предотвратить перемещение бегунка в указанную точку.</span><span class="sxs-lookup"><span data-stu-id="9c61d-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c61d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c61d-114">Remarks</span></span>

<span data-ttu-id="9c61d-115">Отправьте это уведомление клиентам, которые не прослушивают сообщения [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="9c61d-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c61d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9c61d-116">Requirements</span></span>



| <span data-ttu-id="9c61d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9c61d-117">Requirement</span></span> | <span data-ttu-id="9c61d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9c61d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c61d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c61d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c61d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c61d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c61d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c61d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c61d-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c61d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c61d-123">Header</span><span class="sxs-lookup"><span data-stu-id="9c61d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c61d-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c61d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






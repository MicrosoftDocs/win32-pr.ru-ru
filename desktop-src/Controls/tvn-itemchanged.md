---
title: Код уведомления TVN_ITEMCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892005"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="ff0a6-105">\_Код уведомления ТВН итемчанжед</span><span class="sxs-lookup"><span data-stu-id="ff0a6-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="ff0a6-106">Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились.</span><span class="sxs-lookup"><span data-stu-id="ff0a6-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="ff0a6-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0a6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ff0a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff0a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff0a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0a6-110">Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую измененный элемент.</span><span class="sxs-lookup"><span data-stu-id="ff0a6-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="ff0a6-111">Для элемента **учанжед** задано состояние твиф \_ .</span><span class="sxs-lookup"><span data-stu-id="ff0a6-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0a6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff0a6-112">Return value</span></span>

<span data-ttu-id="ff0a6-113">Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.</span><span class="sxs-lookup"><span data-stu-id="ff0a6-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0a6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ff0a6-114">Requirements</span></span>



| <span data-ttu-id="ff0a6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ff0a6-115">Requirement</span></span> | <span data-ttu-id="ff0a6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ff0a6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0a6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff0a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0a6-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff0a6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff0a6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff0a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0a6-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff0a6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff0a6-121">Header</span><span class="sxs-lookup"><span data-stu-id="ff0a6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff0a6-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff0a6-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ff0a6-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ff0a6-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ff0a6-124">**ТВН \_ ИТЕМЧАНЖЕДВ** (Юникод) и **ТВН \_ итемчанжеда** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ff0a6-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ff0a6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff0a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0a6-126">ТВН \_ итемчангинг</span><span class="sxs-lookup"><span data-stu-id="ff0a6-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 






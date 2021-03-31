---
title: Код уведомления TVN_ITEMEXPANDED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента развернут или свернут. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137410"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="7f6cb-105">\_Код уведомления ТВН итемекспандед</span><span class="sxs-lookup"><span data-stu-id="7f6cb-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="7f6cb-106">Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента развернут или свернут.</span><span class="sxs-lookup"><span data-stu-id="7f6cb-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="7f6cb-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6cb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="7f6cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f6cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f6cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f6cb-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="7f6cb-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="7f6cb-111">Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения о родительском элементе в членах **хитем**, **State** и **lParam** .</span><span class="sxs-lookup"><span data-stu-id="7f6cb-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="7f6cb-112">Член **действия** указывает, развернут ли список или свернут.</span><span class="sxs-lookup"><span data-stu-id="7f6cb-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="7f6cb-113">Список возможных значений см. в описании сообщения [**TVM \_ expand**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6cb-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6cb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f6cb-114">Return value</span></span>

<span data-ttu-id="7f6cb-115">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7f6cb-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6cb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7f6cb-116">Requirements</span></span>



| <span data-ttu-id="7f6cb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7f6cb-117">Requirement</span></span> | <span data-ttu-id="7f6cb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7f6cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6cb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f6cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6cb-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f6cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f6cb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f6cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6cb-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f6cb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f6cb-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f6cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f6cb-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6cb-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7f6cb-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7f6cb-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f6cb-126">**ТВН \_ ИТЕМЕКСПАНДЕДВ** (Юникод) и **ТВН \_ итемекспандеда** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7f6cb-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7f6cb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f6cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6cb-128">ТВН \_ итемекспандинг</span><span class="sxs-lookup"><span data-stu-id="7f6cb-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 






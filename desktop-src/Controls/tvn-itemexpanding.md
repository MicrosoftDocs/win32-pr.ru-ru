---
title: Код уведомления TVN_ITEMEXPANDING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента собирается развернуть или свернуть. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989278"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="402c5-105">\_Код уведомления ТВН итемекспандинг</span><span class="sxs-lookup"><span data-stu-id="402c5-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="402c5-106">Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента собирается развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="402c5-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="402c5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="402c5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="402c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="402c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="402c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="402c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="402c5-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="402c5-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="402c5-111">Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения о родительском элементе в членах **хитем**, **State** и **lParam** .</span><span class="sxs-lookup"><span data-stu-id="402c5-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="402c5-112">Член **действия** указывает, следует ли развернуть или свернуть список.</span><span class="sxs-lookup"><span data-stu-id="402c5-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="402c5-113">Список возможных значений см. в описании сообщения [**TVM \_ expand**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="402c5-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="402c5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="402c5-114">Return value</span></span>

<span data-ttu-id="402c5-115">Возвращает **значение true** , чтобы предотвратить расширение или свертывание списка.</span><span class="sxs-lookup"><span data-stu-id="402c5-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="402c5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="402c5-116">Requirements</span></span>



| <span data-ttu-id="402c5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="402c5-117">Requirement</span></span> | <span data-ttu-id="402c5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="402c5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="402c5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="402c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="402c5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="402c5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="402c5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="402c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="402c5-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="402c5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="402c5-123">Header</span><span class="sxs-lookup"><span data-stu-id="402c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="402c5-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="402c5-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="402c5-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="402c5-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="402c5-126">**ТВН \_ ИТЕМЕКСПАНДИНГВ** (Юникод) и **ТВН \_ итемекспандинга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="402c5-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="402c5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="402c5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402c5-128">ТВН \_ итемекспандед</span><span class="sxs-lookup"><span data-stu-id="402c5-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 






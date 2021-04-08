---
title: Код уведомления TVN_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления, что инициируется операция перетаскивания с использованием левой кнопки мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892006"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="c193e-105">\_Код уведомления ТВН бегиндраг</span><span class="sxs-lookup"><span data-stu-id="c193e-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="c193e-106">Сообщает родительскому окну элемента управления иерархического представления, что инициируется операция перетаскивания с использованием левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="c193e-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="c193e-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c193e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="c193e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c193e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c193e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c193e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c193e-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="c193e-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="c193e-111">Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения об элементе, который перетаскивается в элементы **хитем**, **State** и **lParam** .</span><span class="sxs-lookup"><span data-stu-id="c193e-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="c193e-112">Элемент **птдраг** указывает текущие экранные координаты мыши.</span><span class="sxs-lookup"><span data-stu-id="c193e-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c193e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c193e-113">Return value</span></span>

<span data-ttu-id="c193e-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c193e-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c193e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c193e-115">Remarks</span></span>

<span data-ttu-id="c193e-116">Элемент управления "дерево-представление", имеющий стиль [**\_ Дисабледрагдроп "телевизоры**](tree-view-control-window-styles.md) ", не отправляет этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="c193e-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c193e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c193e-117">Requirements</span></span>



| <span data-ttu-id="c193e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c193e-118">Requirement</span></span> | <span data-ttu-id="c193e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c193e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c193e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c193e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c193e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c193e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c193e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c193e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c193e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c193e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c193e-124">Header</span><span class="sxs-lookup"><span data-stu-id="c193e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c193e-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c193e-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c193e-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c193e-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c193e-127">**ТВН \_ БЕГИНДРАГВ** (Юникод) и **ТВН \_ бегиндрага** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c193e-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 






---
title: Код уведомления TVN_SETDISPINFO (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления, что оно должно обновлять сведения об элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654439"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="83fa1-105">\_Код уведомления ТВН сетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="83fa1-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="83fa1-106">Сообщает родительскому окну элемента управления иерархического представления, что оно должно обновлять сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="83fa1-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="83fa1-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="83fa1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="83fa1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83fa1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83fa1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83fa1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83fa1-110">Указатель на структуру [**нмтвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) , описывающую обновляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="83fa1-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="83fa1-111">Член **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) указывает обновляемый элемент, а элемент **Mask** указывает, какие атрибуты элемента обновляются.</span><span class="sxs-lookup"><span data-stu-id="83fa1-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83fa1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83fa1-112">Return value</span></span>

<span data-ttu-id="83fa1-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="83fa1-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="83fa1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83fa1-114">Remarks</span></span>

<span data-ttu-id="83fa1-115">Если элемент **псзтекст** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение тексткаллбакк LPSTR, элемент управления отправляет это уведомление для задания текста элемента.</span><span class="sxs-lookup"><span data-stu-id="83fa1-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="83fa1-116">В этом случае элемент **Mask** элемента *lParam* будет иметь \_ установленный флаг твиф Text.</span><span class="sxs-lookup"><span data-stu-id="83fa1-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="83fa1-117">Если элемент **иимаже** или **иселектедимаже** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение имажекаллбакк I, элемент управления отправляет это уведомление для получения индекса отображаемого изображения значка.</span><span class="sxs-lookup"><span data-stu-id="83fa1-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="83fa1-118">В этом случае элемент **Mask** параметра *lParam* будет иметь \_ установленный флаг твиф Image или твиф \_ селектедимаже.</span><span class="sxs-lookup"><span data-stu-id="83fa1-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fa1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="83fa1-119">Requirements</span></span>



| <span data-ttu-id="83fa1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="83fa1-120">Requirement</span></span> | <span data-ttu-id="83fa1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="83fa1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83fa1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83fa1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="83fa1-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83fa1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83fa1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83fa1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="83fa1-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83fa1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83fa1-126">Header</span><span class="sxs-lookup"><span data-stu-id="83fa1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="83fa1-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="83fa1-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="83fa1-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="83fa1-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83fa1-129">**ТВН \_ СЕТДИСПИНФОВ** (Юникод) и **ТВН \_ сетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="83fa1-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="83fa1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83fa1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fa1-131">**твитем**</span><span class="sxs-lookup"><span data-stu-id="83fa1-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="83fa1-132">**твитемекс**</span><span class="sxs-lookup"><span data-stu-id="83fa1-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="83fa1-133">ТВН \_ жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="83fa1-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 






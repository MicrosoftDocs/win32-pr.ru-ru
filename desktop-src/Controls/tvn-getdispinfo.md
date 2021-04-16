---
title: Код уведомления TVN_GETDISPINFO (Коммктрл. h)
description: Запрашивает, что родительское окно элемента управления представлением дерева предоставляет сведения, необходимые для отображения или сортировки элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534214"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="a2127-105">\_Код уведомления ТВН жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="a2127-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="a2127-106">Запрашивает, что родительское окно элемента управления представлением дерева предоставляет сведения, необходимые для отображения или сортировки элемента.</span><span class="sxs-lookup"><span data-stu-id="a2127-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="a2127-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a2127-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a2127-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2127-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2127-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2127-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2127-110">Указатель на структуру [**нмтвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="a2127-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="a2127-111">Элемент **Item** является структурой [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , члены **маски**, **хитем**, **State** и **lParam** которой определяют требуемый тип информации.</span><span class="sxs-lookup"><span data-stu-id="a2127-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="a2127-112">Необходимо заполнить элементы структуры соответствующими данными.</span><span class="sxs-lookup"><span data-stu-id="a2127-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2127-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2127-113">Return value</span></span>

<span data-ttu-id="a2127-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a2127-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2127-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2127-115">Remarks</span></span>

<span data-ttu-id="a2127-116">Этот код уведомления отправляется в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="a2127-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="a2127-117">Если элемент **псзтекст** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение тексткаллбакк LPSTR, элемент управления отправляет этот код уведомления для получения текста элемента.</span><span class="sxs-lookup"><span data-stu-id="a2127-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="a2127-118">В этом случае элемент **Mask** элемента *lParam* будет иметь \_ установленный флаг твиф Text.</span><span class="sxs-lookup"><span data-stu-id="a2127-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="a2127-119">Если элемент **иимаже** или **иселектедимаже** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение имажекаллбакк I, элемент управления отправляет этот код уведомления для получения индекса значков элемента в списке изображений элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a2127-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="a2127-120">В этом случае, если элемент выбран, для элемента **Mask** параметра *lParam* будет \_ установлен флаг твиф селектедимаже.</span><span class="sxs-lookup"><span data-stu-id="a2127-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="a2127-121">Если элемент не выбран, для элемента **Mask** параметра *lParam* будет \_ установлен флаг образа твиф.</span><span class="sxs-lookup"><span data-stu-id="a2127-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="a2127-122">Если элемент **кчилдрен** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение чилдренкаллбакк I, элемент управления отправляет этот код уведомления для получения значения, указывающего, имеет ли элемент дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="a2127-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="a2127-123">В этом случае для элемента **Mask** параметра *lParam* будет \_ установлен флаг Children твиф.</span><span class="sxs-lookup"><span data-stu-id="a2127-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2127-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a2127-124">Requirements</span></span>



| <span data-ttu-id="a2127-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a2127-125">Requirement</span></span> | <span data-ttu-id="a2127-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a2127-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2127-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2127-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a2127-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2127-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2127-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2127-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a2127-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2127-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2127-131">Header</span><span class="sxs-lookup"><span data-stu-id="a2127-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2127-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2127-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a2127-133">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a2127-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2127-134">**ТВН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ТВН \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2127-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a2127-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2127-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2127-136">ТВН \_ сетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="a2127-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 






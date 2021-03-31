---
title: Сообщение TVM_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для элемента представления дерева и указывает, является ли элемент видимым. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемрект TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Элементы управления Windows для TVM_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135695"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="f8d9a-105">\_Сообщение TVM жетитемрект</span><span class="sxs-lookup"><span data-stu-id="f8d9a-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="f8d9a-106">Извлекает ограничивающий прямоугольник для элемента представления дерева и указывает, является ли элемент видимым.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="f8d9a-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемрект TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="f8d9a-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8d9a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8d9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8d9a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d9a-110">Значение, указывающее часть элемента, для которого необходимо извлечь ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="f8d9a-111">Если этот параметр имеет **значение true**, ограничивающий прямоугольник включает только текст элемента.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="f8d9a-112">В противном случае он включает всю строку, занимаемую элементом в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="f8d9a-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="f8d9a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8d9a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d9a-114">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая при отправке сообщения содержит маркер элемента, для которого извлекается прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="f8d9a-115">Дополнительные сведения о том, как разместить маркер элемента в этом параметре, см. в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="f8d9a-116">После возврата из сообщения этот параметр содержит ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="f8d9a-117">Координаты задаются относительно левого верхнего угла элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="f8d9a-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d9a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8d9a-118">Return value</span></span>

<span data-ttu-id="f8d9a-119">Если элемент является видимым и ограничивающий прямоугольник был успешно извлечен, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="f8d9a-120">В противном случае сообщение возвращает **значение false** и не извлекает ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8d9a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8d9a-121">Remarks</span></span>

<span data-ttu-id="f8d9a-122">При отправке этого сообщения параметр *lParam* содержит маркер элемента, для которого извлекается прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f8d9a-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="f8d9a-123">Этот обработчик помещается в *lParam* , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="f8d9a-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="f8d9a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f8d9a-124">Requirements</span></span>



| <span data-ttu-id="f8d9a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f8d9a-125">Requirement</span></span> | <span data-ttu-id="f8d9a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d9a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d9a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8d9a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d9a-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8d9a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8d9a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8d9a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d9a-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8d9a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8d9a-131">Header</span><span class="sxs-lookup"><span data-stu-id="f8d9a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8d9a-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d9a-132"><dt>Commctrl.h</dt></span></span> </dl> |



 


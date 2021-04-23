---
title: Сообщение TVM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент и все его дочерние элементы из элемента управления представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса DeleteItem TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Элементы управления Windows для TVM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490845"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="a09d7-105">\_Сообщение TVM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="a09d7-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="a09d7-106">Удаляет элемент и все его дочерние элементы из элемента управления представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="a09d7-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="a09d7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ DeleteItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="a09d7-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a09d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a09d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a09d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a09d7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a09d7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a09d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a09d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a09d7-112">**Хтриитем** для удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a09d7-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="a09d7-113">Если параметру *lParam* присвоено значение Тви \_ root или **null**, удаляются все элементы.</span><span class="sxs-lookup"><span data-stu-id="a09d7-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="a09d7-114">Для удаления всех элементов можно также использовать макрос [**\_ делетеаллитемс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="a09d7-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09d7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a09d7-115">Return value</span></span>

<span data-ttu-id="a09d7-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a09d7-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a09d7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a09d7-117">Remarks</span></span>

<span data-ttu-id="a09d7-118">Удалять элементы в ответ на уведомление, например [ТВН \_ селчангинг](tvn-selchanging.md), необязательно.</span><span class="sxs-lookup"><span data-stu-id="a09d7-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="a09d7-119">После удаления элемента его маркер является недопустимым и не может быть использован.</span><span class="sxs-lookup"><span data-stu-id="a09d7-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="a09d7-120">Родительское окно получает код уведомления [ТВН \_ DELETEITEM](tvn-deleteitem.md) при удалении каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="a09d7-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="a09d7-121">Если метка элемента редактируется, операция редактирования отменяется, а родительское окно получает код уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="a09d7-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="a09d7-122">Если удалить все элементы в элементе управления "дерево", у которого есть [**стиль \_ прокрутки "телевизоры**](tree-view-control-window-styles.md) ", элементы, добавленные позднее, могут отображаться неправильно.</span><span class="sxs-lookup"><span data-stu-id="a09d7-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="a09d7-123">Дополнительные сведения см. в разделе [**TreeView \_ делетеаллитемс**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="a09d7-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="a09d7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a09d7-124">Requirements</span></span>



| <span data-ttu-id="a09d7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a09d7-125">Requirement</span></span> | <span data-ttu-id="a09d7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a09d7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a09d7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a09d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a09d7-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a09d7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a09d7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a09d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a09d7-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a09d7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a09d7-131">Header</span><span class="sxs-lookup"><span data-stu-id="a09d7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a09d7-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a09d7-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






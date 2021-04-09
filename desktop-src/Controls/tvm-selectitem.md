---
title: Сообщение TVM_SELECTITEM (Коммктрл. h)
description: Выбирает указанный элемент представления дерева, прокручивает элемент в представлении или перерисовывает элемент в стиле, который используется для указания цели операции перетаскивания.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Элементы управления Windows для TVM_SELECTITEM сообщений
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891597"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="c758f-104">\_Сообщение TVM селектитем</span><span class="sxs-lookup"><span data-stu-id="c758f-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="c758f-105">Выбирает указанный элемент представления дерева, прокручивает элемент в представлении или перерисовывает элемент в стиле, который используется для указания цели операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="c758f-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="c758f-106">Это сообщение можно отправить явным образом или с помощью макроса [**\_ SELECT TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ селектитем**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)или [**TreeView \_ селектдроптаржет**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="c758f-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c758f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c758f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c758f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c758f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c758f-109">Флаг действия.</span><span class="sxs-lookup"><span data-stu-id="c758f-109">Action flag.</span></span> <span data-ttu-id="c758f-110">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c758f-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c758f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c758f-111">Value</span></span></th>
<th><span data-ttu-id="c758f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c758f-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="c758f-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c758f-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c758f-114">Задает выборку для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="c758f-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="c758f-115">Родительское окно элемента управления представлением дерева получает <a href="tvn-selchanging.md">TVN_SELCHANGING</a> и <a href="tvn-selchanged.md">TVN_SELCHANGED</a> коды уведомления.</span><span class="sxs-lookup"><span data-stu-id="c758f-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="c758f-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c758f-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c758f-117">Перерисовывает указанный элемент в стиле, который используется для указания цели операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="c758f-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="c758f-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c758f-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c758f-119">Гарантирует, что указанный элемент является видимым, и, если это возможно, отображает его в верхней части окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c758f-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="c758f-120">Элементы управления "дерево-представление" отображают столько элементов, сколько будет помещаться в окне.</span><span class="sxs-lookup"><span data-stu-id="c758f-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="c758f-121">Если указанный элемент находится ближе к нижней части иерархии элементов управления, он может не стать первым видимым элементом в зависимости от того, сколько элементов умещается в окне.</span><span class="sxs-lookup"><span data-stu-id="c758f-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="c758f-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c758f-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c758f-123">Если выбран один элемент, гарантирует, что TreeView не расширяет его дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="c758f-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="c758f-124">Это допустимо, только если используется с флагом TVGN_CARET.</span><span class="sxs-lookup"><span data-stu-id="c758f-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c758f-125">Чтобы использовать этот флаг, необходимо указать манифест, задающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c758f-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c758f-126">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="c758f-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c758f-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c758f-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c758f-128">Обработчик элемента.</span><span class="sxs-lookup"><span data-stu-id="c758f-128">Handle to an item.</span></span> <span data-ttu-id="c758f-129">Если параметр *lParam* имеет **значение NULL**, элементу управления задается значение, не имеющее выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="c758f-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c758f-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c758f-130">Return value</span></span>

<span data-ttu-id="c758f-131">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c758f-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c758f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c758f-132">Remarks</span></span>

<span data-ttu-id="c758f-133">Если указанный элемент является дочерним по отношению к свернутому родительскому элементу, то родительский список дочерних элементов разворачивается для отображения указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="c758f-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="c758f-134">В этом случае родительское окно элемента управления получает коды уведомлений [ТВН \_ Итемекспандинг](tvn-itemexpanding.md) и [ТВН \_ итемекспандед](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="c758f-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="c758f-135">Использование макроса [**\_ Селектитем в TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) эквивалентно отправке **сообщения \_ Селектитем TVM** с параметром *wParam* , равным \_ значению курсора твгн.</span><span class="sxs-lookup"><span data-stu-id="c758f-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="c758f-136">Использование макроса [**\_ Селектдроптаржет в TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) эквивалентно отправке сообщения **TVM \_ селектитем** с параметром *wParam* , равным \_ значению твгн дрофилите.</span><span class="sxs-lookup"><span data-stu-id="c758f-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="c758f-137">Использование [**TreeView \_ селектсетфирствисибле**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) эквивалентно отправке сообщения **TVM \_ селектитем** с параметром *wParam* , установленным в \_ значение твгн фирствисибле.</span><span class="sxs-lookup"><span data-stu-id="c758f-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c758f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="c758f-138">Requirements</span></span>



| <span data-ttu-id="c758f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="c758f-139">Requirement</span></span> | <span data-ttu-id="c758f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="c758f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c758f-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c758f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c758f-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c758f-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c758f-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c758f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c758f-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c758f-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c758f-145">Header</span><span class="sxs-lookup"><span data-stu-id="c758f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c758f-146"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c758f-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






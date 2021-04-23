---
title: Состояния элементов элемента управления Tree-View (Коммктрл. h)
description: В этом разделе перечислены флаги состояния элемента, используемые для указания состояния элемента в элементе управления "дерево-представление".
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657149"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="8f300-103">Состояния элементов элемента управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="8f300-103">Tree-View Control Item States</span></span>

<span data-ttu-id="8f300-104">В этом разделе перечислены флаги состояния элемента, используемые для указания состояния элемента в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="8f300-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="8f300-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8f300-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="8f300-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8f300-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="8f300-107"><dt>**ТВИС \_ Bold**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="8f300-108">Элемент выделен полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="8f300-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="8f300-109"><dt>**ТВИС \_ Вырезать**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="8f300-110">Элемент выбирается как часть операции вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="8f300-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="8f300-111"><dt>**ТВИС \_ дрофилитед**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="8f300-112">Элемент выбран как цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="8f300-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="8f300-113"><dt>**\_развернутый твис**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="8f300-114">Список дочерних элементов элемента в настоящее время развернут; Это значит, что дочерние элементы видимы.</span><span class="sxs-lookup"><span data-stu-id="8f300-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="8f300-115">Это значение применяется только к родительским элементам.</span><span class="sxs-lookup"><span data-stu-id="8f300-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="8f300-116"><dt>**ТВИС \_ експандедонце**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="8f300-117">Список дочерних элементов элемента был расширен по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="8f300-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="8f300-118">Коды уведомлений [ТВН \_ Итемекспандинг](tvn-itemexpanding.md) и [ТВН \_ итемекспандед](tvn-itemexpanded.md) не формируются для родительских элементов, для которых это состояние задано в ответ на [**сообщение \_ расширения TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="8f300-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="8f300-119">Использование тве \_ сворачивания и тве \_ Коллапсересет с **TVM \_ expand** приведет к сбросу этого состояния.</span><span class="sxs-lookup"><span data-stu-id="8f300-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="8f300-120">Это значение применяется только к родительским элементам.</span><span class="sxs-lookup"><span data-stu-id="8f300-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="8f300-121"><dt>**ТВИС \_ експандпартиал**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="8f300-122">**Версия 4,70**.</span><span class="sxs-lookup"><span data-stu-id="8f300-122">**Version 4.70**.</span></span> <span data-ttu-id="8f300-123">Частично развернутый элемент древовидного представления.</span><span class="sxs-lookup"><span data-stu-id="8f300-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="8f300-124">В этом состоянии видимыми являются только некоторые, но не все дочерние элементы, и отображается символ «плюс» родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="8f300-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="8f300-125"><dt>**ТВИС \_ выбрано**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="8f300-126">Элемент выбран.</span><span class="sxs-lookup"><span data-stu-id="8f300-126">The item is selected.</span></span> <span data-ttu-id="8f300-127">Его внешний вид зависит от того, имеет ли он фокус.</span><span class="sxs-lookup"><span data-stu-id="8f300-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="8f300-128">Элемент будет отображаться с использованием системных цветов для выбора.</span><span class="sxs-lookup"><span data-stu-id="8f300-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="8f300-129"><dt>**ТВИС \_ оверлаймаск**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="8f300-130">Маска для битов, используемых для указания индекса изображения оверлея элемента.</span><span class="sxs-lookup"><span data-stu-id="8f300-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="8f300-131"><dt>**ТВИС \_ статеимажемаск**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="8f300-132">Маска для битов, используемых для указания индекса изображения состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8f300-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="8f300-133"><dt>**ТВИС \_ усермаск**</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="8f300-134">То же, что и **ТВИС \_ статеимажемаск**.</span><span class="sxs-lookup"><span data-stu-id="8f300-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="8f300-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f300-135">Remarks</span></span>

<span data-ttu-id="8f300-136">При установке или извлечении индекса изображения наложения элемента или индекса изображения состояния необходимо указать следующие маски в элементе **статемаск** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :</span><span class="sxs-lookup"><span data-stu-id="8f300-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="8f300-137">**ТВИС \_ оверлаймаск**</span><span class="sxs-lookup"><span data-stu-id="8f300-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="8f300-138">**ТВИС \_ статеимажемаск**</span><span class="sxs-lookup"><span data-stu-id="8f300-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="8f300-139">**ТВИС \_ усермаск**</span><span class="sxs-lookup"><span data-stu-id="8f300-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="8f300-140">Эти значения также можно использовать для маскирования битов состояния, которые не представляют интереса.</span><span class="sxs-lookup"><span data-stu-id="8f300-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f300-141">Требования</span><span class="sxs-lookup"><span data-stu-id="8f300-141">Requirements</span></span>



| <span data-ttu-id="8f300-142">Требование</span><span class="sxs-lookup"><span data-stu-id="8f300-142">Requirement</span></span> | <span data-ttu-id="8f300-143">Значение</span><span class="sxs-lookup"><span data-stu-id="8f300-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f300-144">Header</span><span class="sxs-lookup"><span data-stu-id="8f300-144">Header</span></span><br/> | <dl> <span data-ttu-id="8f300-145"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f300-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






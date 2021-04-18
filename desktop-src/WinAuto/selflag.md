---
title: Константы СЕЛФЛАГ (Олеакк. h)
description: В этом разделе описываются константные значения, используемые для указания способа выбора доступного объекта или фокуса.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717911"
---
# <a name="selflag-constants"></a><span data-ttu-id="bb065-103">Константы СЕЛФЛАГ</span><span class="sxs-lookup"><span data-stu-id="bb065-103">SELFLAG Constants</span></span>

<span data-ttu-id="bb065-104">В этом разделе описываются константные значения, используемые для указания способа выбора доступного объекта или фокуса.</span><span class="sxs-lookup"><span data-stu-id="bb065-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="bb065-105">Константы определяются в олеакк. h и используются с методом [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .</span><span class="sxs-lookup"><span data-stu-id="bb065-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="bb065-106">Следующие сочетания не допускаются:</span><span class="sxs-lookup"><span data-stu-id="bb065-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="bb065-107">СЕЛФЛАГ \_ аддселектион \| селфлаг \_ ремовеселектион</span><span class="sxs-lookup"><span data-stu-id="bb065-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="bb065-108">СЕЛФЛАГ \_ аддселектион \| селфлаг \_ такеселектион</span><span class="sxs-lookup"><span data-stu-id="bb065-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="bb065-109">СЕЛФЛАГ \_ ремовеселектион \| селфлаг \_ такеселектион</span><span class="sxs-lookup"><span data-stu-id="bb065-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="bb065-110">СЕЛФЛАГ \_ екстендселектион \| селфлаг \_ такеселектион</span><span class="sxs-lookup"><span data-stu-id="bb065-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="bb065-111">**Примечание для клиентов:** Microsoft Active Accessibility не поддерживает выбор текста, содержащегося в элементах управления Edit и Rich Edit, поскольку текст представлен в виде строки в [свойстве Value](value-property.md)объекта.</span><span class="sxs-lookup"><span data-stu-id="bb065-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="bb065-112">Дополнительные сведения о выполнении сложных операций выбора см. в разделе [Выбор дочерних объектов](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bb065-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bb065-113">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="bb065-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bb065-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bb065-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="bb065-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-116">Не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="bb065-116">Performs no action.</span></span> <span data-ttu-id="bb065-117">Microsoft Active Accessibility не изменяет выделенный фрагмент или фокус.</span><span class="sxs-lookup"><span data-stu-id="bb065-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="bb065-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-119">Устанавливает фокус на объект и делает его привязкой к выделенной области.</span><span class="sxs-lookup"><span data-stu-id="bb065-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="bb065-120">Используется сама по себе, этот флаг не изменяет выбор.</span><span class="sxs-lookup"><span data-stu-id="bb065-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="bb065-121">Этот результат аналогичен перемещению фокуса вручную с помощью клавиши со стрелкой, удерживая нажатой клавишу CTRL в проводнике Windows или в любом списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="bb065-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="bb065-122">С объектами, имеющими <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS объединяется со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="bb065-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="bb065-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="bb065-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="bb065-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="bb065-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="bb065-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="bb065-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="bb065-129">При вызове метода <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: аккселект</strong></a> с флагом SELFLAG_TAKEFOCUS для объекта, имеющего <strong>HWND</strong>, флаг вступит в силу только в том случае, если родительский объект уже имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="bb065-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="bb065-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-131">Выбирает объект и удаляет выделение из всех других объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="bb065-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="bb065-132">Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения.</span><span class="sxs-lookup"><span data-stu-id="bb065-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bb065-133">SELFLAG_TAKESELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно щелчку одного элемента в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="bb065-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="bb065-134">Этот флаг не должен сочетаться со следующими флагами:</span><span class="sxs-lookup"><span data-stu-id="bb065-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="bb065-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="bb065-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="bb065-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bb065-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="bb065-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-139">Изменяет выделенный фрагмент таким образом, что все объекты между точкой привязки и этим объектом принимают состояние выбора объекта привязки.</span><span class="sxs-lookup"><span data-stu-id="bb065-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="bb065-140">Если объект точки привязки не выделен, объекты удаляются из выделения.</span><span class="sxs-lookup"><span data-stu-id="bb065-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="bb065-141">Если выбран объект привязки, выбор расширяется, чтобы включить этот объект и все объекты между ними.</span><span class="sxs-lookup"><span data-stu-id="bb065-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="bb065-142">Задайте состояние выбора, объединив этот флаг с SELFLAG_ADDSELECTION или SELFLAG_REMOVESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bb065-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="bb065-143">Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения.</span><span class="sxs-lookup"><span data-stu-id="bb065-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bb065-144">SELFLAG_EXTENDSELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно добавлению элемента к выделению вручную путем нажатия клавиши SHIFT и щелчка невыделенного объекта в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="bb065-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bb065-145">Этот флаг не сочетается с SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bb065-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="bb065-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-147">Добавляет объект к текущему выделению; возможный результат — несмежный выбор.</span><span class="sxs-lookup"><span data-stu-id="bb065-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="bb065-148">Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения.</span><span class="sxs-lookup"><span data-stu-id="bb065-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bb065-149">SELFLAG_ADDSELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно добавлению элемента в выделение вручную путем нажатия клавиши CTRL и щелчка невыделенного объекта в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="bb065-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bb065-150">Этот флаг не сочетается с SELFLAG_REMOVESELECTION или SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bb065-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="bb065-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="bb065-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bb065-152">Удаляет объект из текущего выбора. возможный результат — несмежный выбор.</span><span class="sxs-lookup"><span data-stu-id="bb065-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="bb065-153">Если он не сочетается с SELFLAG_TAKEFOCUS, этот флаг не изменяет фокус или привязку выделения.</span><span class="sxs-lookup"><span data-stu-id="bb065-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bb065-154">SELFLAG_REMOVESELECTION | Сочетание SELFLAG_TAKEFOCUS эквивалентно удалению элемента из выделения вручную путем нажатия клавиши CTRL при щелчке выбранного объекта в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="bb065-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bb065-155">Этот флаг не сочетается с SELFLAG_ADDSELECTION или SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bb065-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="bb065-156">Требования</span><span class="sxs-lookup"><span data-stu-id="bb065-156">Requirements</span></span>



| <span data-ttu-id="bb065-157">Требование</span><span class="sxs-lookup"><span data-stu-id="bb065-157">Requirement</span></span> | <span data-ttu-id="bb065-158">Значение</span><span class="sxs-lookup"><span data-stu-id="bb065-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb065-159">Header</span><span class="sxs-lookup"><span data-stu-id="bb065-159">Header</span></span><br/> | <dl> <span data-ttu-id="bb065-160"><dt>Олеакк. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb065-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb065-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb065-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb065-162">**IAccessible:: Аккселект**</span><span class="sxs-lookup"><span data-stu-id="bb065-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="bb065-163">Выбор дочерних объектов</span><span class="sxs-lookup"><span data-stu-id="bb065-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 






---
description: Интерфейс Иекстендер предоставляет набор основных свойств, которые добавляются в интерфейс элемента управления. Программисты могут использовать эти свойства, как если бы они были частью элемента управления.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Интерфейс Иекстендер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656918"
---
# <a name="iextender-interface"></a><span data-ttu-id="3c3b9-104">Интерфейс Иекстендер</span><span class="sxs-lookup"><span data-stu-id="3c3b9-104">IExtender interface</span></span>

<span data-ttu-id="3c3b9-105">Интерфейс **иекстендер** предоставляет набор основных свойств, которые добавляются в интерфейс элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-105">The **IExtender** interface provides a set of basic properties that are added to the interface of a control.</span></span> <span data-ttu-id="3c3b9-106">Программисты могут использовать эти свойства, как если бы они были частью элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-106">Programmers can use these properties as if they were part of the control.</span></span>

## <a name="members"></a><span data-ttu-id="3c3b9-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="3c3b9-107">Members</span></span>

<span data-ttu-id="3c3b9-108">Интерфейс **иекстендер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3c3b9-108">The **IExtender** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c3b9-109">**Иекстендер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c3b9-109">**IExtender** also has these types of members:</span></span>

-   [<span data-ttu-id="3c3b9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="3c3b9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c3b9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c3b9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c3b9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3c3b9-112">Methods</span></span>

<span data-ttu-id="3c3b9-113">Интерфейс **иекстендер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-113">The **IExtender** interface has these methods.</span></span>



| <span data-ttu-id="3c3b9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3c3b9-114">Method</span></span>                         | <span data-ttu-id="3c3b9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3c3b9-115">Description</span></span>                                    |
|:-------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="3c3b9-116">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="3c3b9-116">**Move**</span></span>](iextender-move.md) | <span data-ttu-id="3c3b9-117">Перемещает Мдиформ, форму или элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-117">Moves an MDIForm, form, or control.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3c3b9-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c3b9-118">Properties</span></span>

<span data-ttu-id="3c3b9-119">Интерфейс **иекстендер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-119">The **IExtender** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3c3b9-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c3b9-120">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c3b9-121">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3c3b9-121">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c3b9-122">Описание</span><span class="sxs-lookup"><span data-stu-id="3c3b9-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3c3b9-123">Выровнять</span><span class="sxs-lookup"><span data-stu-id="3c3b9-123">Align</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c3b9-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-124">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c3b9-125">Возвращает или задает значение, определяющее, отображается ли объект в любом месте формы или в верхней, нижней, левой или правой части формы и автоматически изменяется в соответствии с шириной формы.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-125">Returns or sets a value that determines whether an object is displayed in any size anywhere on a form or whether it is displayed at the top, bottom, left, or right of the form and is automatically sized to fit the width of the form.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3c3b9-126">Константа</span><span class="sxs-lookup"><span data-stu-id="3c3b9-126">Constant</span></span></th>
<th><span data-ttu-id="3c3b9-127">Описание</span><span class="sxs-lookup"><span data-stu-id="3c3b9-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c3b9-128">Вбалигнноне 0</span><span class="sxs-lookup"><span data-stu-id="3c3b9-128">vbAlignNone 0</span></span></td>
<td><span data-ttu-id="3c3b9-129">(По умолчанию в форме, отличной от MDI) Нет — размер и расположение можно задать во время разработки или в коде.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-129">(Default in a non-MDI form) None—size and location can be set at design time or in code.</span></span> <span data-ttu-id="3c3b9-130">Параметр игнорируется, если объект находится в форме MDI.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-130">The setting is ignored if the object is on an MDI form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c3b9-131">Вбалигнтоп 1</span><span class="sxs-lookup"><span data-stu-id="3c3b9-131">vbAlignTop 1</span></span></td>
<td><span data-ttu-id="3c3b9-132">(По умолчанию в форме MDI) Top — объект находится в верхней части формы, а его ширина равна значению свойства Скалевидс формы.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-132">(Default in an MDI form) Top—the object is at the top of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c3b9-133">Вбалигнботтом 2</span><span class="sxs-lookup"><span data-stu-id="3c3b9-133">vbAlignBottom 2</span></span></td>
<td><span data-ttu-id="3c3b9-134">Bottom — объект находится в нижней части формы, а его ширина равна значению свойства Скалевидс в форме.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-134">Bottom—the object is at the bottom of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c3b9-135">Вбалигнлефт 3</span><span class="sxs-lookup"><span data-stu-id="3c3b9-135">vbAlignLeft 3</span></span></td>
<td><span data-ttu-id="3c3b9-136">Left — объект находится слева от формы, а его ширина равна значению свойства Скалевидс формы.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-136">Left—the object is at the left of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c3b9-137">Вбалигнригхт 4</span><span class="sxs-lookup"><span data-stu-id="3c3b9-137">vbAlignRight 4</span></span></td>
<td><span data-ttu-id="3c3b9-138">Справа — объект находится справа от формы, а его ширина равна значению свойства Скалевидс в форме.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-138">Right—the object is at the right of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-139">Контейнер</span><span class="sxs-lookup"><span data-stu-id="3c3b9-139">Container</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c3b9-140">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-141">Возвращает контейнер элемента управления в форме.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-141">Returns the container of a control on a form.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-142">Активировано</span><span class="sxs-lookup"><span data-stu-id="3c3b9-142">Enabled</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-143">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-144">Возвращает или задает значение, определяющее, может ли форма или элемент управления отвечать на создаваемые пользователем события.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-144">Returns or sets a value that determines whether a form or control can respond to user-generated events.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-145">Высота</span><span class="sxs-lookup"><span data-stu-id="3c3b9-145">Height</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-146">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-147">Возвращает или задает высоту объекта.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-147">Returns or sets the height of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-148">HWND</span><span class="sxs-lookup"><span data-stu-id="3c3b9-148">Hwnd</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c3b9-149">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-150">Возвращает маркер для формы или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-150">Returns a handle to a form or control.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-151">Левый</span><span class="sxs-lookup"><span data-stu-id="3c3b9-151">Left</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-152">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-153">Возвращает или задает расстояние между внутренним левым ребром объекта и левым ребром его контейнера.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-153">Returns or sets the distance between the internal left edge of an object and the left edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-154">Имя</span><span class="sxs-lookup"><span data-stu-id="3c3b9-154">Name</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c3b9-155">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-156">Возвращает имя, используемое в коде для задания объекта формы, элемента управления или доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-156">Returns the name used in code to identify a form, control, or data access object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-157">Parent</span><span class="sxs-lookup"><span data-stu-id="3c3b9-157">Parent</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c3b9-158">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-159">Возвращает форму, объект или коллекцию, содержащую элемент управления или другой объект или коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-159">Returns the form, object, or collection that contains a control or another object or collection.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-160">TabStop</span><span class="sxs-lookup"><span data-stu-id="3c3b9-160">TabStop</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-161">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-161">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-162">Возвращает или задает значение, указывающее, может ли пользователь использовать клавишу <strong>Tab</strong> для передачи фокуса объекту.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-162">Returns or sets a value that indicates whether a user can use the <strong>Tab</strong> key to give the focus to an object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-163">Начало</span><span class="sxs-lookup"><span data-stu-id="3c3b9-163">Top</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-164">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-164">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-165">Возвращает или задает расстояние между внутренним верхним краями объекта и верхней границей его контейнера.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-165">Returns or sets the distance between the internal top edge of an object and the top edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-166">Видимый</span><span class="sxs-lookup"><span data-stu-id="3c3b9-166">Visible</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-167">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-167">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-168">Возвращает или задает значение, указывающее, является ли объект видимым или скрытым.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-168">Returns or sets a value that indicates whether an object is visible or hidden.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-169">Ширина</span><span class="sxs-lookup"><span data-stu-id="3c3b9-169">Width</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-170">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3c3b9-170">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="3c3b9-171">Возвращает или задает ширину объекта.</span><span class="sxs-lookup"><span data-stu-id="3c3b9-171">Returns or sets the width of an object.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3c3b9-172">Требования</span><span class="sxs-lookup"><span data-stu-id="3c3b9-172">Requirements</span></span>



| <span data-ttu-id="3c3b9-173">Требование</span><span class="sxs-lookup"><span data-stu-id="3c3b9-173">Requirement</span></span> | <span data-ttu-id="3c3b9-174">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3b9-174">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3b9-175">DLL</span><span class="sxs-lookup"><span data-stu-id="3c3b9-175">DLL</span></span><br/> | <dl> <span data-ttu-id="3c3b9-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b9-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



 

 

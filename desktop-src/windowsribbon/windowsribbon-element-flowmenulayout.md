---
title: Фловменулайаут, элемент
description: Представляет горизонтальный макет с разрывами строк для элементов в коллекции.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Лента Windows для элемента Фловменулайаут
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700767"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="25438-104">Фловменулайаут, элемент</span><span class="sxs-lookup"><span data-stu-id="25438-104">FlowMenuLayout element</span></span>

<span data-ttu-id="25438-105">Представляет горизонтальный макет с разрывами строк для элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="25438-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="25438-106">Использование</span><span class="sxs-lookup"><span data-stu-id="25438-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="25438-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="25438-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25438-108">attribute</span><span class="sxs-lookup"><span data-stu-id="25438-108">Attribute</span></span></th>
<th><span data-ttu-id="25438-109">Тип</span><span class="sxs-lookup"><span data-stu-id="25438-109">Type</span></span></th>
<th><span data-ttu-id="25438-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="25438-110">Required</span></span></th>
<th><span data-ttu-id="25438-111">Описание</span><span class="sxs-lookup"><span data-stu-id="25438-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25438-112"><strong>Столбцы</strong></span><span class="sxs-lookup"><span data-stu-id="25438-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="25438-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="25438-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="25438-114">Нет</span><span class="sxs-lookup"><span data-stu-id="25438-114">No</span></span><br/></td>
<td><span data-ttu-id="25438-115">Указывает количество элементов, отображаемых в одной строке.</span><span class="sxs-lookup"><span data-stu-id="25438-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="25438-116">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="25438-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="25438-117">Любое положительное или отрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="25438-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="25438-118">Значение по умолчанию — <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="25438-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25438-119"><strong>Полосы захвата</strong></span><span class="sxs-lookup"><span data-stu-id="25438-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="25438-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="25438-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="25438-121">Нет</span><span class="sxs-lookup"><span data-stu-id="25438-121">No</span></span><br/></td>
<td><span data-ttu-id="25438-122">Маркер изменения размера, присоединенный к раскрывающемся списке коллекции.</span><span class="sxs-lookup"><span data-stu-id="25438-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="25438-123">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="25438-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="25438-124">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="25438-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="25438-125"><dt><span></span><span></span><strong></strong> Вертикаль</span><span class="sxs-lookup"><span data-stu-id="25438-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="25438-126"><dt><span></span><span></span><strong></strong> Нижне</span><span class="sxs-lookup"><span data-stu-id="25438-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="25438-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25438-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25438-128"><strong>Строки</strong></span><span class="sxs-lookup"><span data-stu-id="25438-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="25438-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="25438-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="25438-130">Нет</span><span class="sxs-lookup"><span data-stu-id="25438-130">No</span></span><br/></td>
<td><span data-ttu-id="25438-131">Указывает число строк элемента, видимых без прокрутки.</span><span class="sxs-lookup"><span data-stu-id="25438-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="25438-132">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="25438-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="25438-133">Любое положительное или отрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="25438-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="25438-134">Значение по умолчанию равно <strong>-1</strong> , что указывает на отображение максимально возможного количества строк элементов.</span><span class="sxs-lookup"><span data-stu-id="25438-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="25438-135">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="25438-135">Child elements</span></span>

<span data-ttu-id="25438-136">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="25438-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="25438-137">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="25438-137">Parent elements</span></span>



| <span data-ttu-id="25438-138">Элемент</span><span class="sxs-lookup"><span data-stu-id="25438-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25438-139">**Дропдовнгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="25438-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="25438-140">**Инриббонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="25438-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="25438-141">**Сплитбуттонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="25438-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="25438-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25438-142">Remarks</span></span>

<span data-ttu-id="25438-143">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="25438-143">Required.</span></span>

<span data-ttu-id="25438-144">Элемент [**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или **фловменулайаут** должен выполняться один раз для каждого элемента [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md), [**инриббонгаллери. менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)или [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="25438-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="25438-145">Элементы упорядочиваются в соответствии со свойствами разрыва строки, присущими атрибутам *Row* и *Column* .</span><span class="sxs-lookup"><span data-stu-id="25438-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="25438-146">Если содержимое превышает длину одной строки, меню разбивает строки, заключает строки и соответствующим образом выровнять содержимое.</span><span class="sxs-lookup"><span data-stu-id="25438-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="25438-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="25438-147">Examples</span></span>

<span data-ttu-id="25438-148">В следующем примере показана базовая разметка для [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="25438-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="25438-149">В этом разделе кода показано объявление элемента управления [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md) со спецификацией **фловменулайаут** .</span><span class="sxs-lookup"><span data-stu-id="25438-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="25438-150">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="25438-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="25438-151">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="25438-151">Minimum supported system</span></span><br/> | <span data-ttu-id="25438-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25438-152">Windows 7</span></span> |
| <span data-ttu-id="25438-153">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="25438-153">Can be empty</span></span>                        | <span data-ttu-id="25438-154">Да</span><span class="sxs-lookup"><span data-stu-id="25438-154">Yes</span></span>       |



 

 






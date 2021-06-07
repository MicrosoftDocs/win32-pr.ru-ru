---
title: Вертикалменулайаут, элемент
description: Представляет вертикальный макет для элементов в коллекции.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Лента Windows для элемента Вертикалменулайаут
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444055"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="2fc8c-104">Вертикалменулайаут, элемент</span><span class="sxs-lookup"><span data-stu-id="2fc8c-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="2fc8c-105">Представляет вертикальный макет для элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="2fc8c-106">Использование</span><span class="sxs-lookup"><span data-stu-id="2fc8c-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="2fc8c-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2fc8c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fc8c-108">attribute</span><span class="sxs-lookup"><span data-stu-id="2fc8c-108">Attribute</span></span></th>
<th><span data-ttu-id="2fc8c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2fc8c-109">Type</span></span></th>
<th><span data-ttu-id="2fc8c-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2fc8c-110">Required</span></span></th>
<th><span data-ttu-id="2fc8c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2fc8c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fc8c-112"><strong>Полосы захвата</strong></span><span class="sxs-lookup"><span data-stu-id="2fc8c-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="2fc8c-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="2fc8c-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="2fc8c-114">Нет</span><span class="sxs-lookup"><span data-stu-id="2fc8c-114">No</span></span><br/></td>
<td><span data-ttu-id="2fc8c-115">Маркер изменения размера, присоединенный к раскрывающемся списке коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="2fc8c-116">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2fc8c-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2fc8c-117">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="2fc8c-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2fc8c-118"><dt><span></span><span></span><strong></strong> Вертикаль</span><span class="sxs-lookup"><span data-stu-id="2fc8c-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="2fc8c-119">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fc8c-120"><strong>исмултиплехигхлигхтинженаблед</strong></span><span class="sxs-lookup"><span data-stu-id="2fc8c-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="2fc8c-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="2fc8c-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="2fc8c-122">Нет</span><span class="sxs-lookup"><span data-stu-id="2fc8c-122">No</span></span><br/></td>
<td><span data-ttu-id="2fc8c-123"><strong>Windows 8 и более поздние версии</strong></span><span class="sxs-lookup"><span data-stu-id="2fc8c-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="2fc8c-124">Выделяет все элементы в списке вплоть до, включая, текущий элемент с курсором мыши (а не только элемент onmouseover).</span><span class="sxs-lookup"><span data-stu-id="2fc8c-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="2fc8c-125">Обычно используется для нескольких функций <strong>отмены</strong> и <strong>повтора</strong> .</span><span class="sxs-lookup"><span data-stu-id="2fc8c-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="2fc8c-126">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="2fc8c-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2fc8c-127"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="2fc8c-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="2fc8c-128">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fc8c-129"><strong>Строки</strong></span><span class="sxs-lookup"><span data-stu-id="2fc8c-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="2fc8c-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2fc8c-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2fc8c-131">Нет</span><span class="sxs-lookup"><span data-stu-id="2fc8c-131">No</span></span><br/></td>
<td><span data-ttu-id="2fc8c-132">Указывает число строк элемента, видимых без прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="2fc8c-133">
<dt><span></span><span></span><strong></strong> (xs: integer)</span><span class="sxs-lookup"><span data-stu-id="2fc8c-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2fc8c-134">Любое положительное или отрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="2fc8c-135">Значение по умолчанию равно <strong>-1</strong> , что указывает на отображение максимально возможного количества строк элементов.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2fc8c-136">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2fc8c-136">Child elements</span></span>

<span data-ttu-id="2fc8c-137">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2fc8c-138">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2fc8c-138">Parent elements</span></span>



| <span data-ttu-id="2fc8c-139">Элемент</span><span class="sxs-lookup"><span data-stu-id="2fc8c-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fc8c-140">**Дропдовнгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="2fc8c-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="2fc8c-141">**Инриббонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="2fc8c-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="2fc8c-142">**Сплитбуттонгаллери. Менулайаут**</span><span class="sxs-lookup"><span data-stu-id="2fc8c-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2fc8c-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="2fc8c-143">Remarks</span></span>

<span data-ttu-id="2fc8c-144">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2fc8c-144">Required.</span></span>

<span data-ttu-id="2fc8c-145">Элемент **вертикалменулайаут** или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md) должен выполняться один раз для каждого элемента [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md), [**инриббонгаллери. менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)или [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc8c-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2fc8c-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="2fc8c-146">Examples</span></span>

<span data-ttu-id="2fc8c-147">В следующем примере показана базовая разметка для элемента **вертикалменулайаут** .</span><span class="sxs-lookup"><span data-stu-id="2fc8c-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="2fc8c-148">В этом разделе кода показаны объявления элементов управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc8c-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="2fc8c-149">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2fc8c-149">Element information</span></span>


- <span data-ttu-id="2fc8c-150">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="2fc8c-150">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="2fc8c-151">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="2fc8c-151">**Can be empty**: Yes</span></span>



 

 






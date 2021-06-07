---
title: Менуграуп, элемент
description: Представляет контейнер элементов управления, отображаемых в коллекции, меню или панели инструментов.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Лента Windows для элемента Менуграуп
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95cbda43fe2f652888a7b84539752b5d671868c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442855"
---
# <a name="menugroup-element"></a><span data-ttu-id="efc08-104">Менуграуп, элемент</span><span class="sxs-lookup"><span data-stu-id="efc08-104">MenuGroup element</span></span>

<span data-ttu-id="efc08-105">Представляет контейнер элементов управления, отображаемых в коллекции, меню или панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="efc08-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="efc08-106">Использование</span><span class="sxs-lookup"><span data-stu-id="efc08-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="efc08-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="efc08-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efc08-108">attribute</span><span class="sxs-lookup"><span data-stu-id="efc08-108">Attribute</span></span></th>
<th><span data-ttu-id="efc08-109">Тип</span><span class="sxs-lookup"><span data-stu-id="efc08-109">Type</span></span></th>
<th><span data-ttu-id="efc08-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="efc08-110">Required</span></span></th>
<th><span data-ttu-id="efc08-111">Описание</span><span class="sxs-lookup"><span data-stu-id="efc08-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efc08-112"><strong>Класс</strong></span><span class="sxs-lookup"><span data-stu-id="efc08-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="efc08-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="efc08-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="efc08-114">Нет</span><span class="sxs-lookup"><span data-stu-id="efc08-114">No</span></span><br/></td>
<td><span data-ttu-id="efc08-115">Задает размер и стиль макета для элементов в пользовательском интерфейсе меню.</span><span class="sxs-lookup"><span data-stu-id="efc08-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="efc08-116">Ресурс изображения может быть представлен в двух размерах (крупный и маленький) и связан с элементом в разметке с помощью элементов свойств <a href="windowsribbon-element-command-largeimages.md"><strong>Command. ларжеимажес</strong></a> и <a href="windowsribbon-element-command-smallimages.md"><strong>Command. смаллимажес</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="efc08-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="efc08-117">Если предоставляется только один образ, платформа при необходимости изменяет ее размер.</span><span class="sxs-lookup"><span data-stu-id="efc08-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="efc08-118">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="efc08-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="efc08-119">
<dt><span></span><span></span><strong></strong> (Стандардитемс)</span><span class="sxs-lookup"><span data-stu-id="efc08-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="efc08-120">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efc08-120">Default.</span></span> <br/> <span data-ttu-id="efc08-121">Стиль: небольшое изображение и невыделенный текст.</span><span class="sxs-lookup"><span data-stu-id="efc08-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="efc08-122"><dt><span></span><span></span><strong></strong> (Мажоритемс)</span><span class="sxs-lookup"><span data-stu-id="efc08-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="efc08-123">Стиль: крупный рисунок и полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="efc08-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="efc08-124">Если <strong>менуграуп</strong> является дочерним элементом <a href="windowsribbon-element-applicationmenu.md"><strong>Аппликатионмену</strong></a>, атрибут <em>класса</em> не учитывается и стиль <code>MajorItems</code> применяется платформой.</span><span class="sxs-lookup"><span data-stu-id="efc08-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efc08-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="efc08-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="efc08-126">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="efc08-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="efc08-127">Нет</span><span class="sxs-lookup"><span data-stu-id="efc08-127">No</span></span><br/></td>
<td><span data-ttu-id="efc08-128">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="efc08-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="efc08-129">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="efc08-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="efc08-130">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="efc08-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="efc08-131">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="efc08-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="efc08-132">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="efc08-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="efc08-133">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="efc08-133">Child elements</span></span>



| <span data-ttu-id="efc08-134">Элемент</span><span class="sxs-lookup"><span data-stu-id="efc08-134">Element</span></span>                                                                             | <span data-ttu-id="efc08-135">Описание</span><span class="sxs-lookup"><span data-stu-id="efc08-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="efc08-136">**Button**</span><span class="sxs-lookup"><span data-stu-id="efc08-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="efc08-137">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-138">**Установка**</span><span class="sxs-lookup"><span data-stu-id="efc08-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="efc08-139">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="efc08-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="efc08-141">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="efc08-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="efc08-143">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-144">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="efc08-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="efc08-145">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-146">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="efc08-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="efc08-147">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-148">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="efc08-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="efc08-149">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="efc08-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="efc08-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="efc08-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="efc08-151">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-152">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="efc08-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="efc08-153">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="efc08-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="efc08-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="efc08-155">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="efc08-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="efc08-156">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="efc08-156">Parent elements</span></span>



| <span data-ttu-id="efc08-157">Элемент</span><span class="sxs-lookup"><span data-stu-id="efc08-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efc08-158">**аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="efc08-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="efc08-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="efc08-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="efc08-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="efc08-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="efc08-161">**Дропдовнгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="efc08-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="efc08-162">**Инриббонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="efc08-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="efc08-163">**минитулбар**</span><span class="sxs-lookup"><span data-stu-id="efc08-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="efc08-164">**SplitButton. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="efc08-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="efc08-165">**Сплитбуттонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="efc08-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="efc08-166">Remarks</span><span class="sxs-lookup"><span data-stu-id="efc08-166">Remarks</span></span>

<span data-ttu-id="efc08-167">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="efc08-167">Required.</span></span>

<span data-ttu-id="efc08-168">Должен быть хотя бы один раз для каждого элемента [**аппликатионмену**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)или [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="efc08-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="efc08-169">Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, **менуграуп** ограничивается следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="efc08-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="efc08-170">Если [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md)или [**сплитбуттонгаллери. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) является родительским элементом, **MenuGroup** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="efc08-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="efc08-171">Если [**минитулбар**](windowsribbon-element-minitoolbar.md) является родительским элементом, **менуграуп** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**фонтконтрол**](windowsribbon-element-fontcontrol.md) [**,,**](windowsribbon-element-spinner.md) [**SplitButton**](windowsribbon-element-splitbutton.md), [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="efc08-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="efc08-172">Атрибут Class не требуется, если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="efc08-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="efc08-173">Платформа применяет значение Мажоритемс для атрибута класса.</span><span class="sxs-lookup"><span data-stu-id="efc08-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="efc08-174">Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, атрибут Class не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="efc08-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="efc08-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="efc08-175">Examples</span></span>

<span data-ttu-id="efc08-176">В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом **менуграуп** .</span><span class="sxs-lookup"><span data-stu-id="efc08-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="efc08-177">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с большим и небольшим ресурсом изображения.</span><span class="sxs-lookup"><span data-stu-id="efc08-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="efc08-178">Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="efc08-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="efc08-179">В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с `StandardItems` и `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="efc08-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="efc08-180">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="efc08-180">Element information</span></span>

* <span data-ttu-id="efc08-181">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="efc08-181">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="efc08-182">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="efc08-182">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="efc08-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efc08-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc08-184">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="efc08-184">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="efc08-185">Группа меню</span><span class="sxs-lookup"><span data-stu-id="efc08-185">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 






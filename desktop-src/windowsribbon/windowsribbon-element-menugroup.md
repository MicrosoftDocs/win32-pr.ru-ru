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
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787483"
---
# <a name="menugroup-element"></a><span data-ttu-id="5c73e-104">Менуграуп, элемент</span><span class="sxs-lookup"><span data-stu-id="5c73e-104">MenuGroup element</span></span>

<span data-ttu-id="5c73e-105">Представляет контейнер элементов управления, отображаемых в коллекции, меню или панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="5c73e-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="5c73e-106">Использование</span><span class="sxs-lookup"><span data-stu-id="5c73e-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="5c73e-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5c73e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c73e-108">attribute</span><span class="sxs-lookup"><span data-stu-id="5c73e-108">Attribute</span></span></th>
<th><span data-ttu-id="5c73e-109">Тип</span><span class="sxs-lookup"><span data-stu-id="5c73e-109">Type</span></span></th>
<th><span data-ttu-id="5c73e-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5c73e-110">Required</span></span></th>
<th><span data-ttu-id="5c73e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5c73e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c73e-112"><strong>Класс</strong></span><span class="sxs-lookup"><span data-stu-id="5c73e-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="5c73e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c73e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="5c73e-114">Нет</span><span class="sxs-lookup"><span data-stu-id="5c73e-114">No</span></span><br/></td>
<td><span data-ttu-id="5c73e-115">Задает размер и стиль макета для элементов в пользовательском интерфейсе меню.</span><span class="sxs-lookup"><span data-stu-id="5c73e-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="5c73e-116">Ресурс изображения может быть представлен в двух размерах (крупный и маленький) и связан с элементом в разметке с помощью элементов свойств <a href="windowsribbon-element-command-largeimages.md"><strong>Command. ларжеимажес</strong></a> и <a href="windowsribbon-element-command-smallimages.md"><strong>Command. смаллимажес</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5c73e-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="5c73e-117">Если предоставляется только один образ, платформа при необходимости изменяет ее размер.</span><span class="sxs-lookup"><span data-stu-id="5c73e-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="5c73e-118">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5c73e-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="5c73e-119">
<dt><span></span><span></span><strong></strong> (Стандардитемс)</span><span class="sxs-lookup"><span data-stu-id="5c73e-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="5c73e-120">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c73e-120">Default.</span></span> <br/> <span data-ttu-id="5c73e-121">Стиль: небольшое изображение и невыделенный текст.</span><span class="sxs-lookup"><span data-stu-id="5c73e-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="5c73e-122"><dt><span></span><span></span><strong></strong> (Мажоритемс)</span><span class="sxs-lookup"><span data-stu-id="5c73e-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="5c73e-123">Стиль: крупный рисунок и полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="5c73e-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c73e-124">Если <strong>менуграуп</strong> является дочерним элементом <a href="windowsribbon-element-applicationmenu.md"><strong>Аппликатионмену</strong></a>, атрибут <em>класса</em> не учитывается и стиль <code>MajorItems</code> применяется платформой.</span><span class="sxs-lookup"><span data-stu-id="5c73e-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c73e-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="5c73e-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="5c73e-126">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="5c73e-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="5c73e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="5c73e-127">No</span></span><br/></td>
<td><span data-ttu-id="5c73e-128">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5c73e-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="5c73e-129">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="5c73e-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5c73e-130">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="5c73e-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="5c73e-131">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="5c73e-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="5c73e-132">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="5c73e-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5c73e-133">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5c73e-133">Child elements</span></span>



| <span data-ttu-id="5c73e-134">Элемент</span><span class="sxs-lookup"><span data-stu-id="5c73e-134">Element</span></span>                                                                             | <span data-ttu-id="5c73e-135">Описание</span><span class="sxs-lookup"><span data-stu-id="5c73e-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5c73e-136">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="5c73e-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="5c73e-137">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-138">**Установка**</span><span class="sxs-lookup"><span data-stu-id="5c73e-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="5c73e-139">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="5c73e-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="5c73e-141">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="5c73e-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="5c73e-143">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-144">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="5c73e-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="5c73e-145">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-146">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="5c73e-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="5c73e-147">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-148">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="5c73e-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="5c73e-149">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="5c73e-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="5c73e-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="5c73e-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="5c73e-151">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-152">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="5c73e-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="5c73e-153">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c73e-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="5c73e-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="5c73e-155">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="5c73e-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5c73e-156">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5c73e-156">Parent elements</span></span>



| <span data-ttu-id="5c73e-157">Элемент</span><span class="sxs-lookup"><span data-stu-id="5c73e-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c73e-158">**аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="5c73e-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="5c73e-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="5c73e-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="5c73e-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="5c73e-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="5c73e-161">**Дропдовнгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="5c73e-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="5c73e-162">**Инриббонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="5c73e-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="5c73e-163">**минитулбар**</span><span class="sxs-lookup"><span data-stu-id="5c73e-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="5c73e-164">**SplitButton. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="5c73e-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="5c73e-165">**Сплитбуттонгаллери. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="5c73e-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5c73e-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c73e-166">Remarks</span></span>

<span data-ttu-id="5c73e-167">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5c73e-167">Required.</span></span>

<span data-ttu-id="5c73e-168">Должен быть хотя бы один раз для каждого элемента [**аппликатионмену**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)или [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="5c73e-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="5c73e-169">Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, **менуграуп** ограничивается следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="5c73e-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="5c73e-170">Если [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md)или [**сплитбуттонгаллери. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) является родительским элементом, **MenuGroup** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="5c73e-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="5c73e-171">Если [**минитулбар**](windowsribbon-element-minitoolbar.md) является родительским элементом, **менуграуп** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**фонтконтрол**](windowsribbon-element-fontcontrol.md) [**,,**](windowsribbon-element-spinner.md) [**SplitButton**](windowsribbon-element-splitbutton.md), [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="5c73e-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="5c73e-172">Атрибут Class не требуется, если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="5c73e-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="5c73e-173">Платформа применяет значение Мажоритемс для атрибута класса.</span><span class="sxs-lookup"><span data-stu-id="5c73e-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="5c73e-174">Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, атрибут Class не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5c73e-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="5c73e-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="5c73e-175">Examples</span></span>

<span data-ttu-id="5c73e-176">В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом **менуграуп** .</span><span class="sxs-lookup"><span data-stu-id="5c73e-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="5c73e-177">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с большим и небольшим ресурсом изображения.</span><span class="sxs-lookup"><span data-stu-id="5c73e-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="5c73e-178">Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="5c73e-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



<span data-ttu-id="5c73e-179">В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с `StandardItems` и `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="5c73e-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5c73e-180">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5c73e-180">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5c73e-181">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="5c73e-181">Minimum supported system</span></span><br/> | <span data-ttu-id="5c73e-182">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c73e-182">Windows 7</span></span> |
| <span data-ttu-id="5c73e-183">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="5c73e-183">Can be empty</span></span>                        | <span data-ttu-id="5c73e-184">Нет</span><span class="sxs-lookup"><span data-stu-id="5c73e-184">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="5c73e-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c73e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c73e-186">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="5c73e-186">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="5c73e-187">Группа меню</span><span class="sxs-lookup"><span data-stu-id="5c73e-187">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 






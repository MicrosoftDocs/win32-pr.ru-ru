---
title: Элемент ComboBox
description: Представляет элемент управления "поле со списком".
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Лента Windows для элемента ComboBox
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105700799"
---
# <a name="combobox-element"></a><span data-ttu-id="230bd-104">Элемент ComboBox</span><span class="sxs-lookup"><span data-stu-id="230bd-104">ComboBox element</span></span>

<span data-ttu-id="230bd-105">Представляет элемент управления ["поле со списком"](windowsribbon-controls-combobox.md) .</span><span class="sxs-lookup"><span data-stu-id="230bd-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="230bd-106">Использование</span><span class="sxs-lookup"><span data-stu-id="230bd-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="230bd-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="230bd-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="230bd-108">attribute</span><span class="sxs-lookup"><span data-stu-id="230bd-108">Attribute</span></span></th>
<th><span data-ttu-id="230bd-109">Тип</span><span class="sxs-lookup"><span data-stu-id="230bd-109">Type</span></span></th>
<th><span data-ttu-id="230bd-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="230bd-110">Required</span></span></th>
<th><span data-ttu-id="230bd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="230bd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="230bd-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="230bd-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="230bd-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="230bd-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="230bd-114">Нет</span><span class="sxs-lookup"><span data-stu-id="230bd-114">No</span></span><br/></td>
<td><span data-ttu-id="230bd-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="230bd-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="230bd-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="230bd-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="230bd-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="230bd-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="230bd-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="230bd-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="230bd-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="230bd-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="230bd-120"><strong>исаутокомплетинаблед</strong></span><span class="sxs-lookup"><span data-stu-id="230bd-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="230bd-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="230bd-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="230bd-122">Нет</span><span class="sxs-lookup"><span data-stu-id="230bd-122">No</span></span><br/></td>
<td><span data-ttu-id="230bd-123">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="230bd-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="230bd-124">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="230bd-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="230bd-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="230bd-125">Default.</span></span> <br/> </dd> <span data-ttu-id="230bd-126"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="230bd-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="230bd-127"><strong>Редактирование</strong></span><span class="sxs-lookup"><span data-stu-id="230bd-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="230bd-128">Логическое</span><span class="sxs-lookup"><span data-stu-id="230bd-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="230bd-129">Нет</span><span class="sxs-lookup"><span data-stu-id="230bd-129">No</span></span><br/></td>
<td><span data-ttu-id="230bd-130">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="230bd-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="230bd-131">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="230bd-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="230bd-132">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="230bd-132">Default.</span></span> <br/> </dd> <span data-ttu-id="230bd-133"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="230bd-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="230bd-134"><strong>ресизетипе</strong></span><span class="sxs-lookup"><span data-stu-id="230bd-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="230bd-135">комбобоксресизетипе</span><span class="sxs-lookup"><span data-stu-id="230bd-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="230bd-136">Нет</span><span class="sxs-lookup"><span data-stu-id="230bd-136">No</span></span><br/></td>
<td><span data-ttu-id="230bd-137"><dt><span></span><span></span><strong></strong> (Норесизе)</span><span class="sxs-lookup"><span data-stu-id="230bd-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="230bd-138">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="230bd-138">Default.</span></span> <br/> </dd> <span data-ttu-id="230bd-139"><dt><span></span><span></span><strong></strong> (Вертикалресизе)</span><span class="sxs-lookup"><span data-stu-id="230bd-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="230bd-140">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="230bd-140">Child elements</span></span>

<span data-ttu-id="230bd-141">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="230bd-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="230bd-142">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="230bd-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="230bd-143">Элемент</span><span class="sxs-lookup"><span data-stu-id="230bd-143">Element</span></span></th>
<th><span data-ttu-id="230bd-144">Описание</span><span class="sxs-lookup"><span data-stu-id="230bd-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="230bd-145"><a href="windowsribbon-element-controlgroup.md"><strong>контролграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="230bd-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="230bd-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>дропдовнгаллери</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="230bd-148"><a href="windowsribbon-element-group.md"><strong>Группа</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="230bd-149"><a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="230bd-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="230bd-151">Windows 8 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="230bd-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="230bd-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>сплитбуттонгаллери</strong></a></span><span class="sxs-lookup"><span data-stu-id="230bd-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="230bd-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="230bd-153">Remarks</span></span>

<span data-ttu-id="230bd-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="230bd-154">Optional.</span></span>

<span data-ttu-id="230bd-155">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="230bd-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="230bd-156">Поскольку **ComboBox** является исключительно коллекцией элементов, он не поддерживает командные элементы.</span><span class="sxs-lookup"><span data-stu-id="230bd-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="230bd-157">Он также является единственным элементом управления "Коллекция", который не поддерживает пространство команд (набор команд, объявленных в разметке и перечисленных в нижней части коллекции элементов или коллекции команд).</span><span class="sxs-lookup"><span data-stu-id="230bd-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="230bd-158">Дополнительные сведения см. в разделе [Работа с галереями](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="230bd-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="230bd-159">На следующем снимке экрана показан элемент управления [поля со списком](windowsribbon-controls-combobox.md) ленты в Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="230bd-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![снимок экрана элемента управления ComboBox на ленте Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="230bd-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="230bd-161">Examples</span></span>

<span data-ttu-id="230bd-162">В следующих примерах демонстрируется базовая разметка для **поля со списком**.</span><span class="sxs-lookup"><span data-stu-id="230bd-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="230bd-163">В этом разделе кода показаны объявления команд **ComboBox** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="230bd-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="230bd-164">В этом разделе кода показаны объявления элементов управления **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="230bd-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="230bd-165">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="230bd-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="230bd-166">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="230bd-166">Minimum supported system</span></span><br/> | <span data-ttu-id="230bd-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="230bd-167">Windows 7</span></span> |
| <span data-ttu-id="230bd-168">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="230bd-168">Can be empty</span></span>                        | <span data-ttu-id="230bd-169">Да</span><span class="sxs-lookup"><span data-stu-id="230bd-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="230bd-170">См. также</span><span class="sxs-lookup"><span data-stu-id="230bd-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230bd-171">Элемент управления "Поле со списком"</span><span class="sxs-lookup"><span data-stu-id="230bd-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="230bd-172">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="230bd-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 






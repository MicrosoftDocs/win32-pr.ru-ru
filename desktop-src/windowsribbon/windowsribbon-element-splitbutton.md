---
title: Элемент SplitButton
description: Представляет стандартный элемент управления "кнопка разворачивающейся кнопки".
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Лента для элемента SplitButton Windows
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700885"
---
# <a name="splitbutton-element"></a><span data-ttu-id="1f9f7-104">Элемент SplitButton</span><span class="sxs-lookup"><span data-stu-id="1f9f7-104">SplitButton element</span></span>

<span data-ttu-id="1f9f7-105">Представляет стандартный элемент управления ["кнопка разворачивающейся кнопки"](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9f7-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="1f9f7-106">Использование</span><span class="sxs-lookup"><span data-stu-id="1f9f7-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="1f9f7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1f9f7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f9f7-108">attribute</span><span class="sxs-lookup"><span data-stu-id="1f9f7-108">Attribute</span></span></th>
<th><span data-ttu-id="1f9f7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="1f9f7-109">Type</span></span></th>
<th><span data-ttu-id="1f9f7-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1f9f7-110">Required</span></span></th>
<th><span data-ttu-id="1f9f7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1f9f7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f9f7-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="1f9f7-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="1f9f7-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="1f9f7-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="1f9f7-114">Нет</span><span class="sxs-lookup"><span data-stu-id="1f9f7-114">No</span></span><br/></td>
<td><span data-ttu-id="1f9f7-115">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="1f9f7-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="1f9f7-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1f9f7-117">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="1f9f7-118">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="1f9f7-119">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f9f7-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1f9f7-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1f9f7-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="1f9f7-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1f9f7-122">Нет</span><span class="sxs-lookup"><span data-stu-id="1f9f7-122">No</span></span><br/></td>
<td><span data-ttu-id="1f9f7-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1f9f7-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="1f9f7-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1f9f7-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1f9f7-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1f9f7-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1f9f7-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1f9f7-128">Child elements</span></span>



| <span data-ttu-id="1f9f7-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="1f9f7-129">Element</span></span>                                                                                   | <span data-ttu-id="1f9f7-130">Описание</span><span class="sxs-lookup"><span data-stu-id="1f9f7-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="1f9f7-131">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="1f9f7-132">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-133">**Установка**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="1f9f7-134">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="1f9f7-136">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-137">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="1f9f7-138">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-139">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="1f9f7-140">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="1f9f7-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="1f9f7-142">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-143">**SplitButton. Буттонитем**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="1f9f7-144">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="1f9f7-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="1f9f7-145">**SplitButton. Менуграупс**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="1f9f7-146">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="1f9f7-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="1f9f7-147">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="1f9f7-148">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1f9f7-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="1f9f7-150">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1f9f7-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1f9f7-151">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1f9f7-151">Parent elements</span></span>



| <span data-ttu-id="1f9f7-152">Элемент</span><span class="sxs-lookup"><span data-stu-id="1f9f7-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1f9f7-153">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="1f9f7-154">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="1f9f7-155">**Группа**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="1f9f7-156">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="1f9f7-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="1f9f7-158">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1f9f7-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f9f7-159">Remarks</span></span>

<span data-ttu-id="1f9f7-160">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-160">Optional.</span></span>

<span data-ttu-id="1f9f7-161">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), **SplitButton** или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9f7-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="1f9f7-162">**SplitButton** поддерживает [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложения.</span><span class="sxs-lookup"><span data-stu-id="1f9f7-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="1f9f7-163">[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) и [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) не являются допустимыми дочерними элементами [**DropDownButton**](windowsribbon-element-dropdownbutton.md) , если **DropDownButton** является потомком [**аппликатионмену**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="1f9f7-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="1f9f7-164">[**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md) должен быть выполнен один раз, если следующие элементы отсутствуют в качестве дочерних элементов **SplitButton**:</span><span class="sxs-lookup"><span data-stu-id="1f9f7-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="1f9f7-165">**Переключатель**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="1f9f7-166">**Установка**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="1f9f7-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="1f9f7-168">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="1f9f7-169">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="1f9f7-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-170">**SplitButton**</span></span>
-   [<span data-ttu-id="1f9f7-171">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="1f9f7-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="1f9f7-173">Эти элементы управления обрабатываются как дочерние элементы одного элемента по умолчанию [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9f7-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="1f9f7-174">Примеры</span><span class="sxs-lookup"><span data-stu-id="1f9f7-174">Examples</span></span>

<span data-ttu-id="1f9f7-175">В следующем примере показана базовая разметка для [кнопки Split](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="1f9f7-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="1f9f7-176">В этом разделе кода показаны объявления команд **SplitButton** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="1f9f7-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="1f9f7-177">В этом разделе кода показаны объявления элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="1f9f7-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1f9f7-178">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1f9f7-178">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="1f9f7-179">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1f9f7-179">Minimum supported system</span></span><br/> | <span data-ttu-id="1f9f7-180">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f9f7-180">Windows 7</span></span> |
| <span data-ttu-id="1f9f7-181">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1f9f7-181">Can be empty</span></span>                        | <span data-ttu-id="1f9f7-182">Нет</span><span class="sxs-lookup"><span data-stu-id="1f9f7-182">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="1f9f7-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f9f7-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9f7-184">Элемент управления "разворачивающаяся кнопка"</span><span class="sxs-lookup"><span data-stu-id="1f9f7-184">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="1f9f7-185">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="1f9f7-185">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


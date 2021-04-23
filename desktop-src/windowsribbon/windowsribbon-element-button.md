---
title: Элемент Button (платформа Windows Ribbon)
description: Представляет элемент управления "Кнопка".
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Элемент кнопки "лента" Windows
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133939"
---
# <a name="button-element"></a><span data-ttu-id="f506b-104">Button, элемент</span><span class="sxs-lookup"><span data-stu-id="f506b-104">Button element</span></span>

<span data-ttu-id="f506b-105">Представляет элемент управления ["Кнопка"](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="f506b-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="f506b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="f506b-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="f506b-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f506b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f506b-108">attribute</span><span class="sxs-lookup"><span data-stu-id="f506b-108">Attribute</span></span></th>
<th><span data-ttu-id="f506b-109">Тип</span><span class="sxs-lookup"><span data-stu-id="f506b-109">Type</span></span></th>
<th><span data-ttu-id="f506b-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f506b-110">Required</span></span></th>
<th><span data-ttu-id="f506b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f506b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f506b-112"><strong>Аппликатиондефаултс. Check</strong></span><span class="sxs-lookup"><span data-stu-id="f506b-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="f506b-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="f506b-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="f506b-114">Нет</span><span class="sxs-lookup"><span data-stu-id="f506b-114">No</span></span><br/></td>
<td><span data-ttu-id="f506b-115">Этот атрибут допустим, только если элемент <strong>Button</strong> является дочерним элементом <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f506b-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="f506b-116">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f506b-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="f506b-117">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="f506b-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="f506b-118">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f506b-118">Default.</span></span> <br/> </dd> <span data-ttu-id="f506b-119"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="f506b-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f506b-120"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="f506b-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="f506b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="f506b-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="f506b-122">Нет</span><span class="sxs-lookup"><span data-stu-id="f506b-122">No</span></span><br/></td>
<td><span data-ttu-id="f506b-123">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="f506b-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="f506b-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="f506b-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f506b-125">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="f506b-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="f506b-126">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="f506b-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="f506b-127">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="f506b-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f506b-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f506b-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f506b-129">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="f506b-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f506b-130">Нет</span><span class="sxs-lookup"><span data-stu-id="f506b-130">No</span></span><br/></td>
<td><span data-ttu-id="f506b-131">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f506b-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f506b-132">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="f506b-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f506b-133">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="f506b-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f506b-134">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="f506b-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f506b-135">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="f506b-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f506b-136">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f506b-136">Child elements</span></span>

<span data-ttu-id="f506b-137">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="f506b-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f506b-138">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f506b-138">Parent elements</span></span>



| <span data-ttu-id="f506b-139">Элемент</span><span class="sxs-lookup"><span data-stu-id="f506b-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f506b-140">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="f506b-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="f506b-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f506b-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="f506b-142">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="f506b-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="f506b-143">**Группа**</span><span class="sxs-lookup"><span data-stu-id="f506b-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="f506b-144">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="f506b-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="f506b-145">**Куиккакцесстулбар. Аппликатиондефаултс**</span><span class="sxs-lookup"><span data-stu-id="f506b-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="f506b-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f506b-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="f506b-147">**SplitButton. Буттонитем**</span><span class="sxs-lookup"><span data-stu-id="f506b-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="f506b-148">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="f506b-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="f506b-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f506b-149">Remarks</span></span>

<span data-ttu-id="f506b-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f506b-150">Optional.</span></span>

<span data-ttu-id="f506b-151">Может встречаться не более одного раза для каждого элемента [**SplitButton. буттонитем**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f506b-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="f506b-152">Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f506b-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="f506b-153">**Поддерживает** [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложение.</span><span class="sxs-lookup"><span data-stu-id="f506b-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="f506b-154">Примеры</span><span class="sxs-lookup"><span data-stu-id="f506b-154">Examples</span></span>

<span data-ttu-id="f506b-155">В следующем примере показана базовая разметка для **кнопки**.</span><span class="sxs-lookup"><span data-stu-id="f506b-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="f506b-156">В этом разделе кода показаны объявления команд **кнопки** , а также связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **Button** .</span><span class="sxs-lookup"><span data-stu-id="f506b-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="f506b-157">В этом разделе кода показаны объявления элементов управления **"Кнопка"** .</span><span class="sxs-lookup"><span data-stu-id="f506b-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="f506b-158">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f506b-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f506b-159">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="f506b-159">Minimum supported system</span></span><br/> | <span data-ttu-id="f506b-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f506b-160">Windows 7</span></span> |
| <span data-ttu-id="f506b-161">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="f506b-161">Can be empty</span></span>                        | <span data-ttu-id="f506b-162">Да</span><span class="sxs-lookup"><span data-stu-id="f506b-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="f506b-163">См. также</span><span class="sxs-lookup"><span data-stu-id="f506b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f506b-164">Элемент управления Button</span><span class="sxs-lookup"><span data-stu-id="f506b-164">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="f506b-165">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="f506b-165">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


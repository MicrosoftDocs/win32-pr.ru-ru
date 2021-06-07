---
title: Элемент CheckBox
description: Представляет элемент управления "флажок".
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Лента Windows для элемента CheckBox
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443045"
---
# <a name="checkbox-element"></a><span data-ttu-id="6857b-104">Элемент CheckBox</span><span class="sxs-lookup"><span data-stu-id="6857b-104">CheckBox element</span></span>

<span data-ttu-id="6857b-105">Представляет элемент управления ["флажок"](windowsribbon-controls-checkbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6857b-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="6857b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6857b-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="6857b-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6857b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6857b-108">attribute</span><span class="sxs-lookup"><span data-stu-id="6857b-108">Attribute</span></span></th>
<th><span data-ttu-id="6857b-109">Тип</span><span class="sxs-lookup"><span data-stu-id="6857b-109">Type</span></span></th>
<th><span data-ttu-id="6857b-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6857b-110">Required</span></span></th>
<th><span data-ttu-id="6857b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6857b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6857b-112"><strong>Аппликатиондефаултс. Check</strong></span><span class="sxs-lookup"><span data-stu-id="6857b-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="6857b-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="6857b-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="6857b-114">Нет</span><span class="sxs-lookup"><span data-stu-id="6857b-114">No</span></span><br/></td>
<td><span data-ttu-id="6857b-115">Этот атрибут допустим, только если элемент <strong>CheckBox</strong> является дочерним для <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6857b-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="6857b-116">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6857b-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6857b-117"><strong>Флажок</strong> не поддерживает третичное, или неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="6857b-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="6857b-118">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="6857b-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6857b-119">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6857b-119">Default.</span></span> <br/> </dd> <span data-ttu-id="6857b-120"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="6857b-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6857b-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6857b-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6857b-122">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="6857b-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6857b-123">Нет</span><span class="sxs-lookup"><span data-stu-id="6857b-123">No</span></span><br/></td>
<td><span data-ttu-id="6857b-124">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6857b-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6857b-125">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="6857b-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6857b-126">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="6857b-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6857b-127">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="6857b-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6857b-128">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="6857b-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6857b-129">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6857b-129">Child elements</span></span>

<span data-ttu-id="6857b-130">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="6857b-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6857b-131">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6857b-131">Parent elements</span></span>



| <span data-ttu-id="6857b-132">Элемент</span><span class="sxs-lookup"><span data-stu-id="6857b-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6857b-133">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="6857b-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="6857b-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6857b-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="6857b-135">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="6857b-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="6857b-136">**Группа**</span><span class="sxs-lookup"><span data-stu-id="6857b-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="6857b-137">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="6857b-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="6857b-138">**Куиккакцесстулбар. Аппликатиондефаултс**</span><span class="sxs-lookup"><span data-stu-id="6857b-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="6857b-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6857b-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="6857b-140">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="6857b-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="6857b-141">Remarks</span><span class="sxs-lookup"><span data-stu-id="6857b-141">Remarks</span></span>

<span data-ttu-id="6857b-142">Необязательный или обязательный в зависимости от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="6857b-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="6857b-143">Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6857b-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="6857b-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="6857b-144">Examples</span></span>

<span data-ttu-id="6857b-145">В следующем примере показана базовая разметка для элемента **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="6857b-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="6857b-146">В этом разделе кода показаны объявления команд **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="6857b-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="6857b-147">В этом разделе кода показаны объявления элементов управления **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="6857b-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="6857b-148">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6857b-148">Element information</span></span>

* <span data-ttu-id="6857b-149">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="6857b-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="6857b-150">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="6857b-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="6857b-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6857b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6857b-152">Элемент управления "Флажок"</span><span class="sxs-lookup"><span data-stu-id="6857b-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 






---
title: Контролграуп, элемент
description: Представляет группу элементов управления в шаблоне макета Сизедефинитион.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Лента Windows для элемента Контролграуп
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412425"
---
# <a name="controlgroup-element"></a><span data-ttu-id="54742-104">Контролграуп, элемент</span><span class="sxs-lookup"><span data-stu-id="54742-104">ControlGroup element</span></span>

<span data-ttu-id="54742-105">Представляет группу элементов управления в шаблоне макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="54742-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="54742-106">Использование</span><span class="sxs-lookup"><span data-stu-id="54742-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="54742-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="54742-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54742-108">attribute</span><span class="sxs-lookup"><span data-stu-id="54742-108">Attribute</span></span></th>
<th><span data-ttu-id="54742-109">Тип</span><span class="sxs-lookup"><span data-stu-id="54742-109">Type</span></span></th>
<th><span data-ttu-id="54742-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="54742-110">Required</span></span></th>
<th><span data-ttu-id="54742-111">Описание</span><span class="sxs-lookup"><span data-stu-id="54742-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54742-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="54742-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="54742-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="54742-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="54742-114">Нет</span><span class="sxs-lookup"><span data-stu-id="54742-114">No</span></span><br/></td>
<td><span data-ttu-id="54742-115">Допустим, только если <a href="windowsribbon-element-group.md"><strong>Группа</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="54742-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="54742-116">Каждый <em>SequenceNumber</em> должен быть уникальным в пределах элемента <a href="windowsribbon-element-group.md"><strong>Group</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54742-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="54742-117">Значения для <em>SequenceNumber</em> должны увеличиваться для каждого элемента <strong>Group</strong> , но не должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="54742-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="54742-118">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="54742-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="54742-119">Любое положительное целочисленное значение в диапазоне от 1000 до 59999 включительно.</span><span class="sxs-lookup"><span data-stu-id="54742-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="54742-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="54742-120">Child elements</span></span>



| <span data-ttu-id="54742-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="54742-121">Element</span></span>                                                                                 | <span data-ttu-id="54742-122">Описание</span><span class="sxs-lookup"><span data-stu-id="54742-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="54742-123">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="54742-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="54742-124">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-125">**Установка**</span><span class="sxs-lookup"><span data-stu-id="54742-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="54742-126">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="54742-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="54742-128">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-129">**контролсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="54742-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="54742-130">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="54742-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="54742-132">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-133">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="54742-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="54742-134">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-135">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="54742-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="54742-136">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-137">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="54742-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="54742-138">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="54742-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="54742-139">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="54742-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="54742-140">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="54742-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="54742-142">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="54742-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="54742-144">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-145">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="54742-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="54742-146">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="54742-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="54742-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="54742-148">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="54742-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="54742-149">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="54742-149">Parent elements</span></span>



| <span data-ttu-id="54742-150">Элемент</span><span class="sxs-lookup"><span data-stu-id="54742-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54742-151">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="54742-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="54742-152">**Группа**</span><span class="sxs-lookup"><span data-stu-id="54742-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="54742-153">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="54742-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="54742-154">**Строка**</span><span class="sxs-lookup"><span data-stu-id="54742-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="54742-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54742-155">Remarks</span></span>

<span data-ttu-id="54742-156">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="54742-156">Optional.</span></span>

<span data-ttu-id="54742-157">Может происходить один или несколько раз для каждого элемента [**Group**](windowsribbon-element-group.md) или **контролграуп** .</span><span class="sxs-lookup"><span data-stu-id="54742-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="54742-158">Если порядковые номера не указаны, элементы подготавливаются к просмотру в порядке, указанном в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="54742-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="54742-159">Если [**Group**](windowsribbon-element-group.md) или **контролграуп** является родительским элементом, **контролграуп** ограничивается следующими возможными дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**фонтконтрол**](windowsribbon-element-fontcontrol.md), [**инриббонгаллери**](windowsribbon-element-inribbongallery.md),- [**inner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="54742-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="54742-160">В противном случае, если [**строка**](windowsribbon-element-row.md) или [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) является родителем, [**Группа**](windowsribbon-element-group.md) ограничивается следующим возможным дочерним элементом: [**контролсизедефинитион**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="54742-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54742-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="54742-161">Examples</span></span>

<span data-ttu-id="54742-162">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами [**группы**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="54742-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="54742-163">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="54742-163">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="54742-164">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="54742-164">Minimum supported system</span></span><br/> | <span data-ttu-id="54742-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54742-165">Windows 7</span></span> |
| <span data-ttu-id="54742-166">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="54742-166">Can be empty</span></span>                        | <span data-ttu-id="54742-167">Нет</span><span class="sxs-lookup"><span data-stu-id="54742-167">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="54742-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54742-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54742-169">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="54742-169">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






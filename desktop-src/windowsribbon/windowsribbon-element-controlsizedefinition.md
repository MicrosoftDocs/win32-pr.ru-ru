---
title: Контролсизедефинитион, элемент
description: Представляет стиль макета группы элементов управления в пользовательском шаблоне.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Лента Windows для элемента Контролсизедефинитион
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334176"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="7e224-104">Контролсизедефинитион, элемент</span><span class="sxs-lookup"><span data-stu-id="7e224-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="7e224-105">Представляет стиль макета группы элементов управления в пользовательском шаблоне.</span><span class="sxs-lookup"><span data-stu-id="7e224-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="7e224-106">Использование</span><span class="sxs-lookup"><span data-stu-id="7e224-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="7e224-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7e224-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e224-108">attribute</span><span class="sxs-lookup"><span data-stu-id="7e224-108">Attribute</span></span></th>
<th><span data-ttu-id="7e224-109">Тип</span><span class="sxs-lookup"><span data-stu-id="7e224-109">Type</span></span></th>
<th><span data-ttu-id="7e224-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="7e224-110">Required</span></span></th>
<th><span data-ttu-id="7e224-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7e224-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e224-112"><strong>контролнаме</strong></span><span class="sxs-lookup"><span data-stu-id="7e224-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="7e224-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="7e224-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="7e224-114">Нет</span><span class="sxs-lookup"><span data-stu-id="7e224-114">No</span></span><br/></td>
<td><span data-ttu-id="7e224-115"><dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="7e224-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="7e224-116">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="7e224-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="7e224-117">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="7e224-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="7e224-118">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="7e224-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e224-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="7e224-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="7e224-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="7e224-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="7e224-121">Нет</span><span class="sxs-lookup"><span data-stu-id="7e224-121">No</span></span><br/></td>
<td><span data-ttu-id="7e224-122">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7e224-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="7e224-123">
<dt><span></span><span></span><strong></strong> Достаточ</span><span class="sxs-lookup"><span data-stu-id="7e224-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7e224-124"><dt><span></span><span></span><strong></strong> Значительные</span><span class="sxs-lookup"><span data-stu-id="7e224-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="7e224-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e224-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e224-126"><strong>исимажевисибле</strong></span><span class="sxs-lookup"><span data-stu-id="7e224-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7e224-127">Логическое</span><span class="sxs-lookup"><span data-stu-id="7e224-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="7e224-128">Нет</span><span class="sxs-lookup"><span data-stu-id="7e224-128">No</span></span><br/></td>
<td><span data-ttu-id="7e224-129">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="7e224-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7e224-130">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="7e224-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7e224-131">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e224-131">Default.</span></span> <br/> </dd> <span data-ttu-id="7e224-132"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="7e224-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e224-133"><strong>ислабелвисибле</strong></span><span class="sxs-lookup"><span data-stu-id="7e224-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7e224-134">Логическое</span><span class="sxs-lookup"><span data-stu-id="7e224-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="7e224-135">Нет</span><span class="sxs-lookup"><span data-stu-id="7e224-135">No</span></span><br/></td>
<td><span data-ttu-id="7e224-136">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="7e224-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7e224-137">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="7e224-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7e224-138">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e224-138">Default.</span></span> <br/> </dd> <span data-ttu-id="7e224-139"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="7e224-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e224-140"><strong>Подсказка</strong></span><span class="sxs-lookup"><span data-stu-id="7e224-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="7e224-141">Логическое</span><span class="sxs-lookup"><span data-stu-id="7e224-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="7e224-142">Нет</span><span class="sxs-lookup"><span data-stu-id="7e224-142">No</span></span><br/></td>
<td><span data-ttu-id="7e224-143">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="7e224-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7e224-144">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="7e224-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7e224-145"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="7e224-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7e224-146">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7e224-146">Child elements</span></span>

<span data-ttu-id="7e224-147">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="7e224-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7e224-148">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7e224-148">Parent elements</span></span>



| <span data-ttu-id="7e224-149">Элемент</span><span class="sxs-lookup"><span data-stu-id="7e224-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e224-150">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="7e224-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="7e224-151">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="7e224-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="7e224-152">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7e224-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="7e224-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e224-153">Remarks</span></span>

<span data-ttu-id="7e224-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7e224-154">Optional.</span></span>

<span data-ttu-id="7e224-155">Может происходить один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md)или [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7e224-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="7e224-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e224-156">Examples</span></span>

<span data-ttu-id="7e224-157">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами **контролсизедефинитион** .</span><span class="sxs-lookup"><span data-stu-id="7e224-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="7e224-158">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7e224-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7e224-159">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="7e224-159">Minimum supported system</span></span><br/> | <span data-ttu-id="7e224-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e224-160">Windows 7</span></span> |
| <span data-ttu-id="7e224-161">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="7e224-161">Can be empty</span></span>                        | <span data-ttu-id="7e224-162">Да</span><span class="sxs-lookup"><span data-stu-id="7e224-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="7e224-163">См. также</span><span class="sxs-lookup"><span data-stu-id="7e224-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e224-164">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="7e224-164">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






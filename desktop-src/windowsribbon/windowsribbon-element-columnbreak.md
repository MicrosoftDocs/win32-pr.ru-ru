---
title: Колумнбреак, элемент
description: Представляет вертикальный разделитель (видимый или скрытый) в пользовательских шаблонах макета Сизедефинитион.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Лента Windows для элемента Колумнбреак
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444845"
---
# <a name="columnbreak-element"></a><span data-ttu-id="17812-104">Колумнбреак, элемент</span><span class="sxs-lookup"><span data-stu-id="17812-104">ColumnBreak element</span></span>

<span data-ttu-id="17812-105">Представляет вертикальный разделитель (видимый или скрытый) в пользовательских шаблонах макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="17812-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="17812-106">Использование</span><span class="sxs-lookup"><span data-stu-id="17812-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="17812-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="17812-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17812-108">attribute</span><span class="sxs-lookup"><span data-stu-id="17812-108">Attribute</span></span></th>
<th><span data-ttu-id="17812-109">Тип</span><span class="sxs-lookup"><span data-stu-id="17812-109">Type</span></span></th>
<th><span data-ttu-id="17812-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="17812-110">Required</span></span></th>
<th><span data-ttu-id="17812-111">Описание</span><span class="sxs-lookup"><span data-stu-id="17812-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17812-112"><strong>шовсепаратор</strong></span><span class="sxs-lookup"><span data-stu-id="17812-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="17812-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="17812-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="17812-114">Нет</span><span class="sxs-lookup"><span data-stu-id="17812-114">No</span></span><br/></td>
<td><span data-ttu-id="17812-115">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="17812-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="17812-116">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="17812-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="17812-117">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17812-117">Default.</span></span> <br/> </dd> <span data-ttu-id="17812-118"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="17812-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="17812-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="17812-119">Child elements</span></span>

<span data-ttu-id="17812-120">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="17812-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="17812-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="17812-121">Parent elements</span></span>



| <span data-ttu-id="17812-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="17812-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="17812-123">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="17812-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="17812-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="17812-124">Remarks</span></span>

<span data-ttu-id="17812-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="17812-125">Optional.</span></span>

<span data-ttu-id="17812-126">Может возникать один или несколько раз для каждого элемента [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="17812-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="17812-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="17812-127">Examples</span></span>

<span data-ttu-id="17812-128">В следующем примере показана базовая разметка для элемента **колумнбреак** в шаблоне нестандартного [**сизедефинитион**](windowsribbon-element-sizedefinition.md) макета с четырьмя кнопками.</span><span class="sxs-lookup"><span data-stu-id="17812-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="17812-129">**Колумнбреак** указывается только для `Large` шаблона.</span><span class="sxs-lookup"><span data-stu-id="17812-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="17812-130">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="17812-130">Element information</span></span>

* <span data-ttu-id="17812-131">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="17812-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="17812-132">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="17812-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="17812-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17812-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17812-134">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="17812-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






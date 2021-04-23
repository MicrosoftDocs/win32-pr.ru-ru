---
title: Граупсизедефинитион, элемент
description: Представляет размер макета для группы элементов управления в пользовательском шаблоне.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Лента Windows для элемента Граупсизедефинитион
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700775"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="27929-104">Граупсизедефинитион, элемент</span><span class="sxs-lookup"><span data-stu-id="27929-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="27929-105">Представляет размер макета для группы элементов управления в пользовательском шаблоне.</span><span class="sxs-lookup"><span data-stu-id="27929-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="27929-106">Использование</span><span class="sxs-lookup"><span data-stu-id="27929-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="27929-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="27929-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27929-108">attribute</span><span class="sxs-lookup"><span data-stu-id="27929-108">Attribute</span></span></th>
<th><span data-ttu-id="27929-109">Тип</span><span class="sxs-lookup"><span data-stu-id="27929-109">Type</span></span></th>
<th><span data-ttu-id="27929-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="27929-110">Required</span></span></th>
<th><span data-ttu-id="27929-111">Описание</span><span class="sxs-lookup"><span data-stu-id="27929-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27929-112"><strong>Размер</strong></span><span class="sxs-lookup"><span data-stu-id="27929-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="27929-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="27929-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="27929-114">Нет</span><span class="sxs-lookup"><span data-stu-id="27929-114">No</span></span><br/></td>
<td><span data-ttu-id="27929-115">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="27929-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="27929-116">
<dt><span></span><span></span><strong></strong> Достаточ</span><span class="sxs-lookup"><span data-stu-id="27929-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="27929-117">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27929-117">Default.</span></span> <br/> </dd> <span data-ttu-id="27929-118"><dt><span></span><span></span><strong></strong> Высокое</span><span class="sxs-lookup"><span data-stu-id="27929-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="27929-119"><dt><span></span><span></span><strong></strong> Значительные</span><span class="sxs-lookup"><span data-stu-id="27929-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="27929-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="27929-120">Child elements</span></span>



| <span data-ttu-id="27929-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="27929-121">Element</span></span>                                                                                 | <span data-ttu-id="27929-122">Описание</span><span class="sxs-lookup"><span data-stu-id="27929-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="27929-123">**колумнбреак**</span><span class="sxs-lookup"><span data-stu-id="27929-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="27929-124">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="27929-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="27929-125">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="27929-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="27929-126">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="27929-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="27929-127">**контролсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="27929-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="27929-128">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="27929-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="27929-129">**Строка**</span><span class="sxs-lookup"><span data-stu-id="27929-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="27929-130">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="27929-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="27929-131">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="27929-131">Parent elements</span></span>



| <span data-ttu-id="27929-132">Элемент</span><span class="sxs-lookup"><span data-stu-id="27929-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="27929-133">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="27929-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="27929-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27929-134">Remarks</span></span>

<span data-ttu-id="27929-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="27929-135">Optional.</span></span>

<span data-ttu-id="27929-136">Может возникать до трех раз для каждого элемента [**сизедефинитион**](windowsribbon-element-sizedefinition.md) (один раз для каждого *размера*).</span><span class="sxs-lookup"><span data-stu-id="27929-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="27929-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="27929-137">Examples</span></span>

<span data-ttu-id="27929-138">В следующем примере кода показан базовый пользовательский шаблон, который включает три размера макета группы, которые должны быть определены с помощью элемента **граупсизедефинитион** при создании пользовательского шаблона.</span><span class="sxs-lookup"><span data-stu-id="27929-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="27929-139">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="27929-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="27929-140">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="27929-140">Minimum supported system</span></span><br/> | <span data-ttu-id="27929-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27929-141">Windows 7</span></span> |
| <span data-ttu-id="27929-142">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="27929-142">Can be empty</span></span>                        | <span data-ttu-id="27929-143">Нет</span><span class="sxs-lookup"><span data-stu-id="27929-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="27929-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27929-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27929-145">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="27929-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






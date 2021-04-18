---
title: Row, элемент
description: Представляет строку элементов управления в пользовательском шаблоне макета Сизедефинитион.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Лента для элементов строки
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83a0a5a9e7908cc1c8cff688b3fefc1e8910b6a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710184"
---
# <a name="row-element"></a><span data-ttu-id="539cb-104">Row, элемент</span><span class="sxs-lookup"><span data-stu-id="539cb-104">Row element</span></span>

<span data-ttu-id="539cb-105">Представляет строку элементов управления в пользовательском шаблоне макета Сизедефинитион.</span><span class="sxs-lookup"><span data-stu-id="539cb-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="539cb-106">Использование</span><span class="sxs-lookup"><span data-stu-id="539cb-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="539cb-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="539cb-107">Attributes</span></span>

<span data-ttu-id="539cb-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="539cb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="539cb-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="539cb-109">Child elements</span></span>



| <span data-ttu-id="539cb-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="539cb-110">Element</span></span>                                                                                 | <span data-ttu-id="539cb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="539cb-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="539cb-112">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="539cb-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="539cb-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="539cb-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="539cb-114">**контролсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="539cb-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="539cb-115">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="539cb-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="539cb-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="539cb-116">Parent elements</span></span>



| <span data-ttu-id="539cb-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="539cb-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="539cb-118">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="539cb-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="539cb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="539cb-119">Remarks</span></span>

<span data-ttu-id="539cb-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="539cb-120">Optional.</span></span>

<span data-ttu-id="539cb-121">Может возникать один или несколько раз для каждого элемента [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="539cb-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="539cb-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="539cb-122">Examples</span></span>

<span data-ttu-id="539cb-123">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами **строки** .</span><span class="sxs-lookup"><span data-stu-id="539cb-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="539cb-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="539cb-124">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="539cb-125">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="539cb-125">Minimum supported system</span></span><br/> | <span data-ttu-id="539cb-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="539cb-126">Windows 7</span></span> |
| <span data-ttu-id="539cb-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="539cb-127">Can be empty</span></span>                        | <span data-ttu-id="539cb-128">Нет</span><span class="sxs-lookup"><span data-stu-id="539cb-128">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="539cb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="539cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539cb-130">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="539cb-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






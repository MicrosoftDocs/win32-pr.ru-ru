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
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445025"
---
# <a name="row-element"></a><span data-ttu-id="6d243-104">Row, элемент</span><span class="sxs-lookup"><span data-stu-id="6d243-104">Row element</span></span>

<span data-ttu-id="6d243-105">Представляет строку элементов управления в пользовательском шаблоне макета Сизедефинитион.</span><span class="sxs-lookup"><span data-stu-id="6d243-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="6d243-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6d243-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="6d243-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6d243-107">Attributes</span></span>

<span data-ttu-id="6d243-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="6d243-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6d243-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6d243-109">Child elements</span></span>



| <span data-ttu-id="6d243-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="6d243-110">Element</span></span>                                                                                 | <span data-ttu-id="6d243-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6d243-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6d243-112">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="6d243-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="6d243-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="6d243-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6d243-114">**контролсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="6d243-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="6d243-115">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="6d243-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6d243-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6d243-116">Parent elements</span></span>



| <span data-ttu-id="6d243-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="6d243-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d243-118">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="6d243-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6d243-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="6d243-119">Remarks</span></span>

<span data-ttu-id="6d243-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6d243-120">Optional.</span></span>

<span data-ttu-id="6d243-121">Может возникать один или несколько раз для каждого элемента [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="6d243-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="6d243-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d243-122">Examples</span></span>

<span data-ttu-id="6d243-123">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами **строки** .</span><span class="sxs-lookup"><span data-stu-id="6d243-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6d243-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6d243-124">Element information</span></span>




* <span data-ttu-id="6d243-125">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d243-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="6d243-126">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="6d243-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="6d243-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d243-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d243-128">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="6d243-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






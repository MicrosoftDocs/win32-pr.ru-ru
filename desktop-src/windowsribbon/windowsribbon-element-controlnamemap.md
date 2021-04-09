---
title: Контролнамемап, элемент
description: Представляет контейнер для имен элементов управления в пользовательском шаблоне макета Сизедефинитион.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- Лента Windows для элемента Контролнамемап
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ca5338978be7f9ddf3432cbe1a0fb8d243d8c00
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889655"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="9a215-104">Контролнамемап, элемент</span><span class="sxs-lookup"><span data-stu-id="9a215-104">ControlNameMap element</span></span>

<span data-ttu-id="9a215-105">Представляет контейнер для имен элементов управления в пользовательском шаблоне макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9a215-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="9a215-106">Использование</span><span class="sxs-lookup"><span data-stu-id="9a215-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="9a215-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a215-107">Attributes</span></span>

<span data-ttu-id="9a215-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9a215-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9a215-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a215-109">Child elements</span></span>



| <span data-ttu-id="9a215-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a215-110">Element</span></span>                                                                                 | <span data-ttu-id="9a215-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9a215-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9a215-112">**контролнамедефинитион**</span><span class="sxs-lookup"><span data-stu-id="9a215-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="9a215-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="9a215-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9a215-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9a215-114">Parent elements</span></span>



| <span data-ttu-id="9a215-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a215-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="9a215-116">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="9a215-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9a215-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a215-117">Remarks</span></span>

<span data-ttu-id="9a215-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9a215-118">Optional.</span></span>

<span data-ttu-id="9a215-119">Может встречаться не более одного раза для каждого элемента [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9a215-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9a215-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="9a215-120">Examples</span></span>

<span data-ttu-id="9a215-121">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с элементом **контролнамемап** .</span><span class="sxs-lookup"><span data-stu-id="9a215-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="9a215-122">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9a215-122">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9a215-123">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9a215-123">Minimum supported system</span></span><br/> | <span data-ttu-id="9a215-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a215-124">Windows 7</span></span> |
| <span data-ttu-id="9a215-125">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9a215-125">Can be empty</span></span>                        | <span data-ttu-id="9a215-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9a215-126">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="9a215-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a215-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a215-128">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="9a215-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






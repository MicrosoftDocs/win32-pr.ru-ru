---
title: Контролнамедефинитион, элемент
description: Представляет имя элемента управления в пользовательском шаблоне макета Сизедефинитион.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- Лента Windows для элемента Контролнамедефинитион
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14ec269ce51b0074b9a03f78aea218b482955d1b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334179"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="95ead-104">Контролнамедефинитион, элемент</span><span class="sxs-lookup"><span data-stu-id="95ead-104">ControlNameDefinition element</span></span>

<span data-ttu-id="95ead-105">Представляет имя элемента управления в пользовательском шаблоне макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="95ead-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="95ead-106">Использование</span><span class="sxs-lookup"><span data-stu-id="95ead-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="95ead-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95ead-107">Attributes</span></span>



| <span data-ttu-id="95ead-108">attribute</span><span class="sxs-lookup"><span data-stu-id="95ead-108">Attribute</span></span>           | <span data-ttu-id="95ead-109">Тип</span><span class="sxs-lookup"><span data-stu-id="95ead-109">Type</span></span>                                       | <span data-ttu-id="95ead-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="95ead-110">Required</span></span>      | <span data-ttu-id="95ead-111">Описание</span><span class="sxs-lookup"><span data-stu-id="95ead-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ead-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="95ead-112">**Name**</span></span><br/> | <span data-ttu-id="95ead-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="95ead-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="95ead-114">Нет</span><span class="sxs-lookup"><span data-stu-id="95ead-114">No</span></span><br/> | <span data-ttu-id="95ead-115"><dt> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="95ead-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="95ead-116">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="95ead-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="95ead-117">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="95ead-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="95ead-118">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="95ead-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="95ead-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95ead-119">Child elements</span></span>



| <span data-ttu-id="95ead-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="95ead-120">Element</span></span>                              | <span data-ttu-id="95ead-121">Описание</span><span class="sxs-lookup"><span data-stu-id="95ead-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="95ead-122">**контролнамедефинитион**</span><span class="sxs-lookup"><span data-stu-id="95ead-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="95ead-123">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="95ead-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="95ead-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95ead-124">Parent elements</span></span>



| <span data-ttu-id="95ead-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="95ead-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="95ead-126">**контролнамемап**</span><span class="sxs-lookup"><span data-stu-id="95ead-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="95ead-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95ead-127">Remarks</span></span>

<span data-ttu-id="95ead-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="95ead-128">Optional.</span></span>

<span data-ttu-id="95ead-129">Может возникать один или несколько раз для каждого элемента [**контролнамемап**](windowsribbon-element-controlnamemap.md) .</span><span class="sxs-lookup"><span data-stu-id="95ead-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="95ead-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="95ead-130">Examples</span></span>

<span data-ttu-id="95ead-131">В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с четырьмя элементами **контролнамедефинитион** .</span><span class="sxs-lookup"><span data-stu-id="95ead-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="95ead-132">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="95ead-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="95ead-133">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="95ead-133">Minimum supported system</span></span><br/> | <span data-ttu-id="95ead-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95ead-134">Windows 7</span></span> |
| <span data-ttu-id="95ead-135">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="95ead-135">Can be empty</span></span>                        | <span data-ttu-id="95ead-136">Нет</span><span class="sxs-lookup"><span data-stu-id="95ead-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="95ead-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95ead-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ead-138">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="95ead-138">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






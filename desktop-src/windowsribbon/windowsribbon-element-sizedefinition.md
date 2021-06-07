---
title: Сизедефинитион, элемент
description: Представляет пользовательский шаблон макета для элементов управления ленты.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Лента Windows для элемента Сизедефинитион
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444805"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="6142c-104">Сизедефинитион, элемент</span><span class="sxs-lookup"><span data-stu-id="6142c-104">SizeDefinition element</span></span>

<span data-ttu-id="6142c-105">Представляет пользовательский шаблон макета для элементов управления ленты.</span><span class="sxs-lookup"><span data-stu-id="6142c-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="6142c-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6142c-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="6142c-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6142c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6142c-108">attribute</span><span class="sxs-lookup"><span data-stu-id="6142c-108">Attribute</span></span></th>
<th><span data-ttu-id="6142c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="6142c-109">Type</span></span></th>
<th><span data-ttu-id="6142c-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6142c-110">Required</span></span></th>
<th><span data-ttu-id="6142c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6142c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6142c-112"><strong>Имя</strong></span><span class="sxs-lookup"><span data-stu-id="6142c-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="6142c-113">xs: Поситивеинтежер или xs: String или xs: Token</span><span class="sxs-lookup"><span data-stu-id="6142c-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="6142c-114">Да</span><span class="sxs-lookup"><span data-stu-id="6142c-114">Yes</span></span><br/></td>
<td><span data-ttu-id="6142c-115">Если <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. сизедефинитионс</strong></a> является родительским элементом, в противном случае — необязательный.</span><span class="sxs-lookup"><span data-stu-id="6142c-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="6142c-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String или xs: token)</span><span class="sxs-lookup"><span data-stu-id="6142c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="6142c-117">Строка или целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="6142c-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="6142c-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="6142c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6142c-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="6142c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6142c-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6142c-120">Child elements</span></span>



| <span data-ttu-id="6142c-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="6142c-121">Element</span></span>                                                                             | <span data-ttu-id="6142c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6142c-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="6142c-123">**контролнамемап**</span><span class="sxs-lookup"><span data-stu-id="6142c-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="6142c-124">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="6142c-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="6142c-125">**граупсизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="6142c-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="6142c-126">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="6142c-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6142c-127">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6142c-127">Parent elements</span></span>



| <span data-ttu-id="6142c-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="6142c-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6142c-129">**Группа**</span><span class="sxs-lookup"><span data-stu-id="6142c-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="6142c-130">**Лента. Сизедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="6142c-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6142c-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="6142c-131">Remarks</span></span>

<span data-ttu-id="6142c-132">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6142c-132">Optional.</span></span>

<span data-ttu-id="6142c-133">Может встречаться не более одного раза для каждого элемента [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="6142c-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="6142c-134">Может происходить один или несколько раз для каждого элемента [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="6142c-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="6142c-135">Стандартные [шаблоны макета](windowsribbon-templates.md) Ribbon Framework указываются с помощью атрибута *сизедефинитион* элемента [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="6142c-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="6142c-136">Если соответствующий элемент [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) не объявлен для каждого элемента [**Group**](windowsribbon-element-group.md) в элементе [**Tab**](windowsribbon-element-tab.md) , возникнет ошибка проверки.</span><span class="sxs-lookup"><span data-stu-id="6142c-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="6142c-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="6142c-137">Examples</span></span>

<span data-ttu-id="6142c-138">В следующем примере кода показан базовый пользовательский шаблон.</span><span class="sxs-lookup"><span data-stu-id="6142c-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6142c-139">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6142c-139">Element information</span></span>


- <span data-ttu-id="6142c-140">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="6142c-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="6142c-141">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="6142c-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="6142c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6142c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6142c-143">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="6142c-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






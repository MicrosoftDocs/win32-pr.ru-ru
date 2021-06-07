---
title: Элемент ScalingPolicy
description: Представляет контейнер для спецификаций масштабирования.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Лента Windows для элемента Скалингполици
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444995"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="56bb5-104">Элемент ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="56bb5-104">ScalingPolicy element</span></span>

<span data-ttu-id="56bb5-105">Представляет контейнер для спецификаций масштабирования.</span><span class="sxs-lookup"><span data-stu-id="56bb5-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="56bb5-106">Использование</span><span class="sxs-lookup"><span data-stu-id="56bb5-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="56bb5-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="56bb5-107">Attributes</span></span>

<span data-ttu-id="56bb5-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="56bb5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="56bb5-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="56bb5-109">Child elements</span></span>



| <span data-ttu-id="56bb5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="56bb5-110">Element</span></span>                                                                                       | <span data-ttu-id="56bb5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="56bb5-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="56bb5-112">**Масштабирование**</span><span class="sxs-lookup"><span data-stu-id="56bb5-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="56bb5-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="56bb5-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="56bb5-114">**Скалингполици. Идеалсизес**</span><span class="sxs-lookup"><span data-stu-id="56bb5-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="56bb5-115">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="56bb5-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="56bb5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="56bb5-116">Parent elements</span></span>



| <span data-ttu-id="56bb5-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="56bb5-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="56bb5-118">**TAB. Скалингполици**</span><span class="sxs-lookup"><span data-stu-id="56bb5-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="56bb5-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="56bb5-119">Remarks</span></span>

<span data-ttu-id="56bb5-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="56bb5-120">Required.</span></span>

<span data-ttu-id="56bb5-121">Должен выполняться один раз для каждой [**вкладки. скалингполици**](windowsribbon-element-tab-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56bb5-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="56bb5-122">Элемент **скалингполици** содержит манифест для объявлений [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) и [**Scale**](windowsribbon-element-scale.md) , задающих параметры адаптивного макета для одного или нескольких элементов [**группы**](windowsribbon-element-group.md) при изменении размера ленты.</span><span class="sxs-lookup"><span data-stu-id="56bb5-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="56bb5-123">Список объявлений [**масштаба**](windowsribbon-element-scale.md) должен быть в порядке убывания допустимых размеров (крупные, средние, небольшие, всплывающие) для [**сизедефинитион**](windowsribbon-element-sizedefinition.md) , связанного с элементом [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="56bb5-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="56bb5-124">Настоятельно рекомендуется указать соответствующую политику масштабирования таким образом, чтобы лента могла быть отображена без полос прокрутки при изменении размера на 300 пикселей в 96 точек на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="56bb5-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="56bb5-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="56bb5-125">Examples</span></span>

<span data-ttu-id="56bb5-126">В следующем примере показано, как можно настроить внешний вид элементов управления в [**группе**](windowsribbon-element-group.md) с помощью функции адаптивного макета в шаблонах ленты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="56bb5-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="56bb5-127">В манифесте **скалингполици** в этом примере задается предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.</span><span class="sxs-lookup"><span data-stu-id="56bb5-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="56bb5-128">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="56bb5-128">Element information</span></span>

- <span data-ttu-id="56bb5-129">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="56bb5-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="56bb5-130">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="56bb5-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="56bb5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56bb5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bb5-132">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="56bb5-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: Скалингполици. Идеалсизес, свойство
description: Представляет контейнер спецификаций масштабирования для предпочтительного шаблона Сизедефинитион на основе размера ленты.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Лента Windows для свойства Скалингполици. Идеалсизес
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701073"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="90492-104">Скалингполици. Идеалсизес, свойство</span><span class="sxs-lookup"><span data-stu-id="90492-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="90492-105">Представляет контейнер спецификаций масштабирования для предпочтительного шаблона [**сизедефинитион**](windowsribbon-element-sizedefinition.md) на основе размера ленты.</span><span class="sxs-lookup"><span data-stu-id="90492-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="90492-106">Использование</span><span class="sxs-lookup"><span data-stu-id="90492-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="90492-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="90492-107">Attributes</span></span>

<span data-ttu-id="90492-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="90492-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="90492-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90492-109">Child elements</span></span>



| <span data-ttu-id="90492-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="90492-110">Element</span></span>                                                 | <span data-ttu-id="90492-111">Описание</span><span class="sxs-lookup"><span data-stu-id="90492-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="90492-112">**Измените**</span><span class="sxs-lookup"><span data-stu-id="90492-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="90492-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="90492-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="90492-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="90492-114">Parent elements</span></span>



| <span data-ttu-id="90492-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="90492-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="90492-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="90492-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="90492-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90492-117">Remarks</span></span>

<span data-ttu-id="90492-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="90492-118">Optional.</span></span>

<span data-ttu-id="90492-119">Может встречаться не более одного раза для каждого [**скалингполици**](windowsribbon-element-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="90492-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="90492-120">Если **скалингполици. идеалсизес** определен, то должна присутствовать запись [**масштабирования**](windowsribbon-element-scale.md) для каждого элемента [**Group**](windowsribbon-element-group.md) в элементе [**Tab**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="90492-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="90492-121">**Скалингполици. идеалсизес** — предпочтительные макеты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для [**группы**](windowsribbon-element-group.md) элементов управления.</span><span class="sxs-lookup"><span data-stu-id="90492-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="90492-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="90492-122">Examples</span></span>

<span data-ttu-id="90492-123">В следующем примере показано, как можно настроить внешний вид элементов управления в [**группе**](windowsribbon-element-group.md) с помощью функции адаптивного макета в шаблонах ленты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="90492-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="90492-124">В манифесте [**скалингполици**](windowsribbon-element-scalingpolicy.md) в этом примере задается предпочтение **скалингполици. идеалсизес** [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.</span><span class="sxs-lookup"><span data-stu-id="90492-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="90492-125">Требования</span><span class="sxs-lookup"><span data-stu-id="90492-125">Requirements</span></span>



| <span data-ttu-id="90492-126">Требование</span><span class="sxs-lookup"><span data-stu-id="90492-126">Requirement</span></span> | <span data-ttu-id="90492-127">Значение</span><span class="sxs-lookup"><span data-stu-id="90492-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="90492-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90492-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90492-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="90492-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="90492-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90492-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90492-131">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="90492-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90492-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90492-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90492-133">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="90492-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






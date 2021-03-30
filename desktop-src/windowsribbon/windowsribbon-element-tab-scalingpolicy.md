---
title: Свойство Tab. Скалингполици
description: Представляет контейнер для спецификаций масштабирования табуляции.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Лента Windows свойства Tab. Скалингполици
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492498"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="fd103-104">Свойство Tab. Скалингполици</span><span class="sxs-lookup"><span data-stu-id="fd103-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="fd103-105">Представляет контейнер для спецификаций масштабирования [табуляции](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="fd103-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="fd103-106">Использование</span><span class="sxs-lookup"><span data-stu-id="fd103-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="fd103-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fd103-107">Attributes</span></span>

<span data-ttu-id="fd103-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fd103-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd103-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fd103-109">Child elements</span></span>



| <span data-ttu-id="fd103-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="fd103-110">Element</span></span>                                                                 | <span data-ttu-id="fd103-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fd103-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="fd103-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="fd103-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="fd103-113">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="fd103-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fd103-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fd103-114">Parent elements</span></span>



| <span data-ttu-id="fd103-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="fd103-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="fd103-116">**TAB**</span><span class="sxs-lookup"><span data-stu-id="fd103-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fd103-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd103-117">Remarks</span></span>

<span data-ttu-id="fd103-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fd103-118">Optional.</span></span>

<span data-ttu-id="fd103-119">Для каждой [**вкладки**](windowsribbon-element-tab.md)может использоваться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="fd103-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="fd103-120">В спецификациях масштабирования описывается поведение размера и макета для элементов управления на [вкладке](windowsribbon-controls-tab.md) при изменении размера ленты.</span><span class="sxs-lookup"><span data-stu-id="fd103-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="fd103-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd103-121">Examples</span></span>

<span data-ttu-id="fd103-122">В следующем примере кода показан манифест [**скалингполици**](windowsribbon-element-scalingpolicy.md) , указывающий предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.</span><span class="sxs-lookup"><span data-stu-id="fd103-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fd103-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fd103-123">Requirements</span></span>



| <span data-ttu-id="fd103-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fd103-124">Requirement</span></span> | <span data-ttu-id="fd103-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fd103-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fd103-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd103-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fd103-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd103-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fd103-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd103-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fd103-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd103-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd103-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd103-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd103-131">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="fd103-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: Элемент Scale
description: Представляет предпочитаемый размер и макет группы элементов управления через пару Group, Сизедефинитион.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Лента Windows для элемента Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412446"
---
# <a name="scale-element"></a><span data-ttu-id="10d18-104">Элемент Scale</span><span class="sxs-lookup"><span data-stu-id="10d18-104">Scale element</span></span>

<span data-ttu-id="10d18-105">Представляет предпочитаемый размер и макет [**группы**](windowsribbon-element-group.md) элементов управления с помощью пары {**Group**, [**сизедефинитион**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="10d18-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="10d18-106">Использование</span><span class="sxs-lookup"><span data-stu-id="10d18-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="10d18-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="10d18-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10d18-108">attribute</span><span class="sxs-lookup"><span data-stu-id="10d18-108">Attribute</span></span></th>
<th><span data-ttu-id="10d18-109">Тип</span><span class="sxs-lookup"><span data-stu-id="10d18-109">Type</span></span></th>
<th><span data-ttu-id="10d18-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10d18-110">Required</span></span></th>
<th><span data-ttu-id="10d18-111">Описание</span><span class="sxs-lookup"><span data-stu-id="10d18-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10d18-112"><strong>Группа</strong></span><span class="sxs-lookup"><span data-stu-id="10d18-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="10d18-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="10d18-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="10d18-114">Да</span><span class="sxs-lookup"><span data-stu-id="10d18-114">Yes</span></span><br/></td>
<td><span data-ttu-id="10d18-115">Должен соответствовать существующей <a href="windowsribbon-element-group.md"><strong>группе</strong></a> <em>CommandName</em>.</span><span class="sxs-lookup"><span data-stu-id="10d18-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="10d18-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="10d18-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="10d18-117">Строка или целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="10d18-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="10d18-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="10d18-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="10d18-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="10d18-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10d18-120"><strong>Размер</strong></span><span class="sxs-lookup"><span data-stu-id="10d18-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="10d18-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="10d18-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="10d18-122">Да</span><span class="sxs-lookup"><span data-stu-id="10d18-122">Yes</span></span><br/></td>
<td><span data-ttu-id="10d18-123">Это значение должно соответствовать одному из допустимых размеров для атрибута <em>сизедефинитион</em> связанной <a href="windowsribbon-element-group.md"><strong>группы</strong></a> элементов управления, указанных в поле <em>Группа</em>.</span><span class="sxs-lookup"><span data-stu-id="10d18-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="10d18-124">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="10d18-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="10d18-125">
<dt><span></span><span></span><strong></strong> Подсказки</span><span class="sxs-lookup"><span data-stu-id="10d18-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="10d18-126">Идентичный макет элемента управления, <code>Large</code> но размещается во всплывающей или раскрывающейся области.</span><span class="sxs-lookup"><span data-stu-id="10d18-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="10d18-127"><dt><span></span><span></span><strong></strong> Значительные</span><span class="sxs-lookup"><span data-stu-id="10d18-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="10d18-128">Шаблон Small <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="10d18-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="10d18-129"><dt><span></span><span></span><strong></strong> Высокое</span><span class="sxs-lookup"><span data-stu-id="10d18-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="10d18-130">Средний шаблон <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="10d18-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="10d18-131"><dt><span></span><span></span><strong></strong> Достаточ</span><span class="sxs-lookup"><span data-stu-id="10d18-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="10d18-132">Крупный шаблон <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="10d18-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="10d18-133">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="10d18-133">Child elements</span></span>

<span data-ttu-id="10d18-134">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="10d18-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="10d18-135">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="10d18-135">Parent elements</span></span>



| <span data-ttu-id="10d18-136">Элемент</span><span class="sxs-lookup"><span data-stu-id="10d18-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10d18-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="10d18-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="10d18-138">**Скалингполици. Идеалсизес**</span><span class="sxs-lookup"><span data-stu-id="10d18-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="10d18-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10d18-139">Remarks</span></span>

<span data-ttu-id="10d18-140">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="10d18-140">Optional.</span></span>

<span data-ttu-id="10d18-141">Может происходить один или несколько раз для каждого [**скалингполици**](windowsribbon-element-scalingpolicy.md) или [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md).</span><span class="sxs-lookup"><span data-stu-id="10d18-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="10d18-142">Каждая пара атрибутов (*Group*, *size*) должна быть уникальной.</span><span class="sxs-lookup"><span data-stu-id="10d18-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="10d18-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="10d18-143">Examples</span></span>

<span data-ttu-id="10d18-144">В следующем примере показано, как можно настроить внешний вид элементов управления в [**группе**](windowsribbon-element-group.md) с помощью функции адаптивного макета в шаблонах ленты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="10d18-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="10d18-145">В манифесте [**скалингполици**](windowsribbon-element-scalingpolicy.md) в этом примере задается предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы **масштаба** задаются для влияния на режим свертывания в порядке убывания размера каждой группы.</span><span class="sxs-lookup"><span data-stu-id="10d18-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="10d18-146">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10d18-146">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="10d18-147">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="10d18-147">Minimum supported system</span></span><br/> | <span data-ttu-id="10d18-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10d18-148">Windows 7</span></span> |
| <span data-ttu-id="10d18-149">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="10d18-149">Can be empty</span></span>                        | <span data-ttu-id="10d18-150">Да</span><span class="sxs-lookup"><span data-stu-id="10d18-150">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="10d18-151">См. также</span><span class="sxs-lookup"><span data-stu-id="10d18-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d18-152">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="10d18-152">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






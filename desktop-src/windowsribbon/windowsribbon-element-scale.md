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
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445015"
---
# <a name="scale-element"></a>Элемент Scale

Представляет предпочитаемый размер и макет [**группы**](windowsribbon-element-group.md) элементов управления с помощью пары {**Group**, [**сизедефинитион**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Использование

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Группа</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Да<br/></td>
<td>Должен соответствовать существующей <a href="windowsribbon-element-group.md"><strong>группе</strong></a> <em>CommandName</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка или целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Размер</strong><br/></td>
<td>xs:string<br/></td>
<td>Да<br/></td>
<td>Это значение должно соответствовать одному из допустимых размеров для атрибута <em>сизедефинитион</em> связанной <a href="windowsribbon-element-group.md"><strong>группы</strong></a> элементов управления, указанных в поле <em>Группа</em>. <br/> Ограничено одним из следующих значений: <br/> <br/>
<dt><span></span><span></span><strong></strong> Подсказки<br/> </dt> <dd> Идентичный макет элемента управления, <code>Large</code> но размещается во всплывающей или раскрывающейся области.<br/> </dd> <dt><span></span><span></span><strong></strong> Значительные<br/> </dt> <dd> Шаблон Small <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .<br/> </dd> <dt><span></span><span></span><strong></strong> Высокое<br/> </dt> <dd> Средний шаблон <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .<br/> </dd> <dt><span></span><span></span><strong></strong> Достаточ<br/> </dt> <dd> Крупный шаблон <a href="windowsribbon-element-sizedefinition.md"><strong>сизедефинитион</strong></a> .<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**Скалингполици. Идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может происходить один или несколько раз для каждого [**скалингполици**](windowsribbon-element-scalingpolicy.md) или [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md).

Каждая пара атрибутов (*Group*, *size*) должна быть уникальной.

## <a name="examples"></a>Примеры

В следующем примере показано, как можно настроить внешний вид элементов управления в [**группе**](windowsribbon-element-group.md) с помощью функции адаптивного макета в шаблонах ленты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

В манифесте [**скалингполици**](windowsribbon-element-scalingpolicy.md) в этом примере задается предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы **масштаба** задаются для влияния на режим свертывания в порядке убывания размера каждой группы.


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



## <a name="element-information"></a>Сведения об элементе



* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: Элемент ScalingPolicy
description: Представляет контейнер для спецификаций масштабирования.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- элемент скалингполици Windows лента
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 202112a24a74c9b20d429910fd0ee9447002ce7f2cb95133165fb968eaaf4f69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007474"
---
# <a name="scalingpolicy-element"></a>Элемент ScalingPolicy

Представляет контейнер для спецификаций масштабирования.

## <a name="usage"></a>Использование

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                       | Описание                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Масштабирование**](windowsribbon-element-scale.md)<br/>                                       | Может происходить один или несколько раз<br/> <br/> |
| [**Скалингполици. Идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                         |
|---------------------------------------------------------------------------------|
| [**TAB. Скалингполици**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен выполняться один раз для каждой [**вкладки. скалингполици**](windowsribbon-element-tab-scalingpolicy.md).

Элемент **скалингполици** содержит манифест для объявлений [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) и [**Scale**](windowsribbon-element-scale.md) , задающих параметры адаптивного макета для одного или нескольких элементов [**группы**](windowsribbon-element-group.md) при изменении размера ленты.

Список объявлений [**масштаба**](windowsribbon-element-scale.md) должен быть в порядке убывания допустимых размеров (крупные, средние, небольшие, всплывающие) для [**сизедефинитион**](windowsribbon-element-sizedefinition.md) , связанного с элементом [**Group**](windowsribbon-element-group.md) .

> [!Note]  
> Настоятельно рекомендуется указать соответствующую политику масштабирования таким образом, чтобы лента могла быть отображена без полос прокрутки при изменении размера на 300 пикселей в 96 точек на дюйм (DPI).

 

## <a name="examples"></a>Примеры

В следующем примере показано, как можно настроить внешний вид элементов управления в [**группе**](windowsribbon-element-group.md) с помощью функции адаптивного макета в шаблонах ленты [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

В манифесте **скалингполици** в этом примере задается предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.


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

- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 






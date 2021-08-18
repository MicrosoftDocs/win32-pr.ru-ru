---
title: Row, элемент
description: Представляет строку элементов управления в пользовательском шаблоне макета Сизедефинитион.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- элемент Row Windows лента
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59913d8a733e4186f2c00e35431d68ebdea839e67103a46873e6f3f64f3a72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449564"
---
# <a name="row-element"></a>Row, элемент

Представляет строку элементов управления в пользовательском шаблоне макета Сизедефинитион.

## <a name="usage"></a>Использование

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                 | Описание                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>                   | Может происходить один или несколько раз<br/> <br/> |
| [**контролсизедефинитион**](windowsribbon-element-controlsizedefinition.md)<br/> | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                             |
|-------------------------------------------------------------------------------------|
| [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может возникать один или несколько раз для каждого элемента [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) .

## <a name="examples"></a>Примеры

В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами **строки** .


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



## <a name="element-information"></a>Сведения об элементе




* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 






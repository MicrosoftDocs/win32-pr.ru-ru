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
ms.openlocfilehash: 6b2dc1db251d4d657c3793d2a66a9add1d324c37
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443445"
---
# <a name="controlnamedefinition-element"></a>Контролнамедефинитион, элемент

Представляет имя элемента управления в пользовательском шаблоне макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

## <a name="usage"></a>Использование

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a>Атрибуты



| attribute           | Тип                                       | Обязательно      | Описание                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Имя**<br/> | xs: Поситивеинтежер или xs: String<br/> | Нет<br/> | <dt> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                              | Описание                                        |
|--------------------------------------|----------------------------------------------------|
| **контролнамедефинитион**<br/> | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                   |
|---------------------------------------------------------------------------|
| [**контролнамемап**](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может возникать один или несколько раз для каждого элемента [**контролнамемап**](windowsribbon-element-controlnamemap.md) .

## <a name="examples"></a>Примеры

В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с четырьмя элементами **контролнамедефинитион** .


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

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 






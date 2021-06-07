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
# <a name="sizedefinition-element"></a>Сизедефинитион, элемент

Представляет пользовательский шаблон макета для элементов управления ленты.

## <a name="usage"></a>Использование

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
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
<td><strong>Имя</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String или xs: Token<br/></td>
<td>Да<br/></td>
<td>Если <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. сизедефинитионс</strong></a> является родительским элементом, в противном случае — необязательный.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String или xs: token)<br/> </dt> <dd> Строка или целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                             | Описание                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**контролнамемап**](windowsribbon-element-controlnamemap.md)<br/>           | Может выполняться не более одного раза<br/> <br/>   |
| [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Группа**](windowsribbon-element-group.md)<br/>                                   |
| [**Лента. Сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**Group**](windowsribbon-element-group.md) .

Может происходить один или несколько раз для каждого элемента [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) .

Стандартные [шаблоны макета](windowsribbon-templates.md) Ribbon Framework указываются с помощью атрибута *сизедефинитион* элемента [**Group**](windowsribbon-element-group.md) .

Если соответствующий элемент [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) не объявлен для каждого элемента [**Group**](windowsribbon-element-group.md) в элементе [**Tab**](windowsribbon-element-tab.md) , возникнет ошибка проверки.

## <a name="examples"></a>Примеры

В следующем примере кода показан базовый пользовательский шаблон.


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


- **Минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 






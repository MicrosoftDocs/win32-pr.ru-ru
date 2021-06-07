---
title: Контролграуп, элемент
description: Представляет группу элементов управления в шаблоне макета Сизедефинитион.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Лента Windows для элемента Контролграуп
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442945"
---
# <a name="controlgroup-element"></a>Контролграуп, элемент

Представляет группу элементов управления в шаблоне макета [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

## <a name="usage"></a>Использование

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
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
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Допустим, только если <a href="windowsribbon-element-group.md"><strong>Группа</strong></a> является родительским элементом.<br/> Каждый <em>SequenceNumber</em> должен быть уникальным в пределах элемента <a href="windowsribbon-element-group.md"><strong>Group</strong></a> . Значения для <em>SequenceNumber</em> должны увеличиваться для каждого элемента <strong>Group</strong> , но не должны быть последовательными. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любое положительное целочисленное значение в диапазоне от 1000 до 59999 включительно.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                 | Описание                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                               | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                           | Может происходить один или несколько раз<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Может происходить один или несколько раз<br/> <br/> |
| [**контролсизедефинитион**](windowsribbon-element-controlsizedefinition.md)<br/> | Может происходить один или несколько раз<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>             | Может происходить один или несколько раз<br/> <br/> |
| [**фонтконтрол**](windowsribbon-element-fontcontrol.md)<br/>                     | Может выполняться не более одного раза<br/> <br/>      |
| [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)<br/>             | Может происходить один или несколько раз<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Может происходить один или несколько раз<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Может происходить один или несколько раз<br/> <br/> |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>       | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                             |
|-------------------------------------------------------------------------------------|
| **контролграуп**<br/>                                                         |
| [**Группа**](windowsribbon-element-group.md)<br/>                             |
| [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Строка**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может происходить один или несколько раз для каждого элемента [**Group**](windowsribbon-element-group.md) или **контролграуп** .

Если порядковые номера не указаны, элементы подготавливаются к просмотру в порядке, указанном в разметке ленты.

Если [**Group**](windowsribbon-element-group.md) или **контролграуп** является родительским элементом, **контролграуп** ограничивается следующими возможными дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**фонтконтрол**](windowsribbon-element-fontcontrol.md), [**инриббонгаллери**](windowsribbon-element-inribbongallery.md),- [**inner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md) .

В противном случае, если [**строка**](windowsribbon-element-row.md) или [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) является родителем, [**Группа**](windowsribbon-element-group.md) ограничивается следующим возможным дочерним элементом: [**контролсизедефинитион**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Примеры

В следующем примере кода показана базовая разметка для пользовательского шаблона макета с четырьмя кнопками [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с различными элементами [**группы**](windowsribbon-element-group.md) .


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

 

 






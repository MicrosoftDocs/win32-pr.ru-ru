---
title: Элемент CheckBox
description: Представляет элемент управления "флажок".
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- элемент CheckBox Windows лента
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754269600c779210e7eee786e3a60262dec06d1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623980"
---
# <a name="checkbox-element"></a>Элемент CheckBox

Представляет элемент управления ["флажок"](windowsribbon-controls-checkbox.md) .

## <a name="usage"></a>Использование

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td><strong>Аппликатиондефаултс. Check</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Этот атрибут допустим, только если элемент <strong>CheckBox</strong> является дочерним для <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>. <br/> Ограничено одним из следующих значений:<br/>
<blockquote>
[!Note]<br />
<strong>Флажок</strong> не поддерживает третичное, или неопределенное состояние.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Группа**](windowsribbon-element-group.md)<br/>                                                                   |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**Куиккакцесстулбар. Аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Remarks

Необязательный или обязательный в зависимости от родительского элемента.

Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **CheckBox** .

В этом разделе кода показаны объявления команд **CheckBox** .


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



В этом разделе кода показаны объявления элементов управления **CheckBox** .


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да


## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления "Флажок"](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 






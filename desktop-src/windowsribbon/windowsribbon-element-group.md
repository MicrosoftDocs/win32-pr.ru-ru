---
title: Group, элемент
description: Представляет элемент управления "Группа", который выступает в качестве контейнера для группы элементов.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- элемент группы Windows лента
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86d12ddb781ecf7e1effba1cade8eb00e92fe20b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631372"
---
# <a name="group-element"></a>Group, элемент

Представляет элемент управления " [Группа](windowsribbon-controls-group.md) ", который выступает в качестве контейнера для группы элементов.

## <a name="usage"></a>Использование

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><strong>аппликатионмодес</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.<br/> Пробелы допустимы и пропускаются.<br/> Максимальная длина: 250 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>сизедефинитион</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>При указании значения <em>сизедефинитион</em> ограничивается одним из <a href="windowsribbon-templates.md">шаблонов макета</a> , определенных платформой Ribbon. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Любая последовательность из нуля или более символов.<br/> Максимальная длина не ограничена.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                             | Описание                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Кнопка**](windowsribbon-element-button.md)<br/>                           | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>         | Может происходить один или несколько раз<br/> <br/> |
| [**фонтконтрол**](windowsribbon-element-fontcontrol.md)<br/>                 | Может выполняться не более одного раза<br/> <br/>      |
| [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)<br/>         | Может происходить один или несколько раз<br/> <br/> |
| [**сизедефинитион**](windowsribbon-element-sizedefinition.md)<br/>           | Может выполняться не более одного раза<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Может происходить один или несколько раз<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Может происходить один или несколько раз<br/> <br/> |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>   | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                             |
|-----------------------------------------------------|
| [**Вкладка**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может происходить один или несколько раз для каждого элемента [**вкладки**](windowsribbon-element-tab.md) .

[**Вкладка**](windowsribbon-element-tab.md) поддерживает [режимы приложений](ribbon-applicationmodes.md).

Разметка Ribbon допустима только в том случае, если дочерние элементы **группы** соответствуют шаблону, указанному для *сизедефинитион*.

## <a name="examples"></a>Примеры

В следующем примере кода показано использование пользовательского шаблона в **группе**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также

<dl> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> <dt>

[Управление группой](windowsribbon-controls-group.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


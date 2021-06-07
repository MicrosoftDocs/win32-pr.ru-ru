---
title: DropDownButton, элемент
description: Представляет стандартный элемент управления "кнопка Drop-Down".
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Лента Windows для элемента DropDownButton
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a42b8ffb6d39c1da8993972c0b25995f778bdaca
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442965"
---
# <a name="dropdownbutton-element"></a>DropDownButton, элемент

Представляет стандартный элемент управления "раскрывающийся [список"](windowsribbon-controls-dropdownbutton.md) .

## <a name="usage"></a>Использование

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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
<td><strong>аппликатионмодес</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.<br/> Пробелы допустимы и пропускаются.<br/> Максимальная длина: 250 символов. <br/> </dd> </dl></td>
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



| Элемент                                                                             | Описание                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| **DropDownButton**<br/>                                                       | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>         | Может происходить один или несколько раз<br/> <br/> |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                     | Должен быть хотя бы один раз<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Может происходить один или несколько раз<br/> <br/> |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>   | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Группа**](windowsribbon-element-group.md)<br/>                           |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный или обязательный в зависимости от родительского элемента.

Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

**DropDownButton** поддерживает [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложения.

[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) и [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) не являются допустимыми дочерними элементами **DropDownButton** , если **DropDownButton** является потомком [**аппликатионмену**](windowsribbon-element-applicationmenu.md).

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для **DropDownButton**.

В этом разделе кода показаны объявления команд **DropDownButton** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **DropDownButton** .


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



В этом разделе кода показаны объявления элементов управления **DropDownButton** .


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления "Кнопка раскрывающегося списка"](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


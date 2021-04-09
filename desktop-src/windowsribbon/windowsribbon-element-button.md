---
title: Элемент Button (платформа Windows Ribbon)
description: Представляет элемент управления "Кнопка".
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Элемент кнопки "лента" Windows
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133939"
---
# <a name="button-element"></a>Button, элемент

Представляет элемент управления ["Кнопка"](windowsribbon-controls-button.md) .

## <a name="usage"></a>Использование

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>Аппликатиондефаултс. Check</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Этот атрибут допустим, только если элемент <strong>Button</strong> является дочерним элементом <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>. <br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>аппликатионмодес</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.<br/> Пробелы допустимы и пропускаются.<br/> Максимальная длина: 250 символов. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
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
| [**SplitButton. Буттонитем**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**SplitButton. буттонитем**](windowsribbon-element-splitbutton-buttonitem.md) .

Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

**Поддерживает** [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложение.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для **кнопки**.

В этом разделе кода показаны объявления команд **кнопки** , а также связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **Button** .


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



В этом разделе кода показаны объявления элементов управления **"Кнопка"** .


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Да       |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления Button](windowsribbon-controls-button.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


---
title: Дропдовнколорпиккер, элемент
description: Представляет Drop-Down цвет, Пиккерконтрол, что при нажатии кнопки отображается палитра цветовых палитр.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- элемент дропдовнколорпиккер Windows лента
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31525ee1b7233f0bf49668856d917ef14bc034b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622890"
---
# <a name="dropdowncolorpicker-element"></a>Дропдовнколорпиккер, элемент

Представляет элемент управления " [Выбор цвета](windowsribbon-controls-dropdowncolorpicker.md)", который при нажатии отображает палитру цветовых палитр.

## <a name="usage"></a>Использование

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
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
<td><strong>чипсизе</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Размер каждой микросхемы или образца цвета. <br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> Значительные<br/> </dt> <dd> Каждая цветовая Микросхема представляет собой 11x11 пиксельный квадрат. <br/> </dd> <dt><span></span><span></span><strong></strong> Высокое<br/> </dt> <dd> Каждая цветовая Микросхема представляет собой пиксельный квадрат размером 16x16 пикселей. <br/> </dd> <dt><span></span><span></span><strong></strong> Достаточ<br/> </dt> <dd> Каждая цветовая Микросхема представляет собой 24x24 пиксельный квадрат. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>колортемплате</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Шаблоны макета, указывающие тип выбора раскрывающегося <a href="windowsribbon-controls-dropdowncolorpicker.md">цвета</a>. <br/> Ограничено одним из следующих значений (если не объявлены дополнительные атрибуты, связанные с <em>колортемплате</em> , отображается представление по умолчанию):<br/> <br/>
<dt><span></span><span></span><strong></strong> (Семеколорс)<br/> </dt> <dd> По умолчанию. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Установка атрибута <em>колортемплате</em> для <code>ThemeColors</code> включения следующих функций:<br/>
<ul>
<li>Привязка SplitButton.</li>
<li>По умолчанию отображается кнопка <strong>автоматического</strong> цвета.</li>
<li>сетка образцов <strong>цветов Windows темы</strong> .</li>
<li>Сетка образцов <strong>стандартных цветов</strong> .</li>
<li>Сетка образцов <strong>последних цветов</strong> необязательна.</li>
<li>Диалоговое окно " <strong>другие цвета</strong> " средство запуска.</li>
<li>По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Стандардколорс)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Установка атрибута <em>колортемплате</em> для <code>StandardColors</code> включения следующих функций:<br/>
<ul>
<li>Привязка SplitButton.</li>
<li>По умолчанию отображается кнопка <strong>автоматического</strong> цвета.</li>
<li>Сетка образцов <strong>стандартных цветов</strong> .</li>
<li>Диалоговое окно " <strong>другие цвета</strong> " средство запуска.</li>
<li>По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Хигхлигхтколорс)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Установка атрибута <em>колортемплате</em> для <code>HighlightColors</code> включения следующих функций:<br/>
<ul>
<li>Привязка SplitButton.</li>
<li>Сетка образцов <strong>стандартных цветов</strong> без заголовка.</li>
<li>По умолчанию не отображается кнопка цвета <strong>цвета</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Столбцы</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Число столбцов цветовой микросхемы (или образцов).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любое положительное целочисленное значение от 1 до 256 включительно.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>исаутоматикколорбуттонвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Отображает (или скрывает) кнопку <strong>автоматического</strong> цвета. <br/> Допустим, только <code>StandardColors</code> Если <code>ThemeColors</code> указан параметр или для атрибута <em>колортемплате</em> . <br/> Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>исноколорбуттонвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Отображает (или скрывает) кнопку <strong>без цвета</strong> . <br/> Допустимо для всех значений <em>колортемплате</em> .<br/> Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>рецентколоргридровс</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Число строк цветовой микросхемы (или образца) в области " <strong>Последние цвета</strong> ". <br/> Допустимо, только если <code>ThemeColors</code> для атрибута <em>колортемплате</em> задано значение.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любое положительное целочисленное значение от 1 до 256 включительно.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>стандардколоргридровс</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Число строк цветовой микросхемы (или образца) в области <strong>Стандартные цвета</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любое положительное целочисленное значение от 1 до 256 включительно.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>семеколоргридровс</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Число строк цветовой микросхемы (или образца) в области <strong>цвета темы</strong> .<br/> Допустимо, только если <code>ThemeColors</code> для атрибута <em>колортемплате</em> задано значение.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любое положительное целочисленное значение от 1 до 256 включительно.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Группа**](windowsribbon-element-group.md)<br/>                           |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для всех трех типов [средства выбора цвета](windowsribbon-controls-dropdowncolorpicker.md)раскрывающегося списка.

В этом разделе кода показаны объявления команд для трех элементов **дропдовнколорпиккер** .


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



В этом разделе кода показаны три типа объявлений элементов управления **дропдовнколорпиккер** .


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления выбора цвета в раскрывающемся списке](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Пример Дропдовнколорпиккер](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 






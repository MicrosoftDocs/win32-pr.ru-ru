---
title: Дропдовнгаллери, элемент
description: Представляет Drop-Down элемент управления "Коллекция" с меню на основе галереи.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- элемент дропдовнгаллери Windows лента
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6926346ef8158930c72a004edf6bb414b9f2d4f2574712f5dd99945d08961cff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393104"
---
# <a name="dropdowngallery-element"></a>Дропдовнгаллери, элемент

Представляет [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления галереи с меню на основе галереи.

## <a name="usage"></a>Использование

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
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
<td>нет<br/></td>
<td>Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.<br/> Пробелы допустимы и пропускаются.<br/> Максимальная длина: 250 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>хасларжеитемс</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Определяет, отображается ли в элементе управления галереи большой или маленький ресурс изображения команды. <br/>
<blockquote>
[!Note]<br />
Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Command</code> .
</blockquote>
<br/> Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>итемхеигхт</strong><br/></td>
<td>xs:integer<br/></td>
<td>нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>итемвидс</strong><br/></td>
<td>xs:integer<br/></td>
<td>нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>текстпоситион</strong><br/></td>
<td>текстпоситионтипе<br/></td>
<td>нет<br/></td>
<td>Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> Нижний<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Ыть<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Слева<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Крывает<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Справа<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Лучшая<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Тип</strong><br/></td>
<td>xs:string<br/></td>
<td>нет<br/></td>
<td>Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> Файлов<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Меню<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                           | Описание                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Кнопка**](windowsribbon-element-button.md)<br/>                                         | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                                     | Может происходить один или несколько раз<br/> <br/> |
| [**Дропдовнгаллери. Менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | Должно выполняться только один раз<br/> <br/>     |
| [**Дропдовнгаллери. Менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>контролграуп</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Группа</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a><br/></td>
<td>Если он содержится в <a href="windowsribbon-element-applicationmenu.md"><strong>аппликатионмену</strong></a>. Этот элемент поддерживается только на первом уровне и не должен иметь дочерних элементов.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 и более поздних версий.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md)или [**SplitButton**](windowsribbon-element-splitbutton.md) .

**Дропдовнгаллери** поддерживает [режимы приложений](ribbon-applicationmodes.md).

на следующем снимке экрана показан [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления "лента" в Microsoft Paint для Windows 7.

![снимок экрана с раскрывающимся элементом управления галереи в Microsoft Paint для Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для **дропдовнгаллери**.

В этом разделе кода показаны объявления команд **дропдовнгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **дропдовнгаллери** .


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



В этом разделе кода показаны объявления элементов управления **дропдовнгаллери** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент управления "раскрывающийся список"**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

 


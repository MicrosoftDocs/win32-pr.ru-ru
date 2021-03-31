---
title: Инриббонгаллери, элемент
description: Представляет коллекцию In-Ribbon, элемент управления на основе галереи, который предоставляет подмножество элементов по умолчанию непосредственно на ленте. Все оставшиеся элементы отображаются при нажатии кнопки раскрывающегося меню.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Лента Windows для элемента Инриббонгаллери
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/30/2020
ms.locfileid: "104069731"
---
# <a name="inribbongallery-element"></a>Инриббонгаллери, элемент

Представляет [коллекцию на ленте](windowsribbon-controls-inribbongallery.md), элемент управления на основе галереи, который предоставляет подмножество элементов по умолчанию непосредственно на ленте. Все оставшиеся элементы отображаются при нажатии кнопки раскрывающегося меню.

## <a name="usage"></a>Использование

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
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
<tr class="odd">
<td><strong>итемхеигхт</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Вместе с <em>итемвидс</em>определяет размер изображения элемента, отображаемого в элементе управления галереи. <br/>
<blockquote>
[!Note]<br />
Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>итемвидс</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Вместе с <em>итемхеигхт</em>определяет размер изображения элемента, отображаемого в элементе управления галереи. <br/>
<blockquote>
[!Note]<br />
Применяется только к коллекциям, в которых значение атрибута <em>Type</em> равно <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>максколумнс</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает максимальное число столбцов, которые отображаются в <strong>инриббонгаллери</strong> , например в раскрывающемся списке <em>крупной</em> группы.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>максколумнсмедиум</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает максимальное число столбцов, которое <strong>инриббонгаллери</strong> отображается в макете группы <em>средних</em> , перед переключением на <em>крупный</em> макет. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает максимальное количество строк для макета элементов <strong>инриббонгаллери</strong> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>минколумнсларже</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает минимальное число столбцов, отображаемых <strong>инриббонгаллери</strong> в макете <em>большой</em> группы перед переключением на <em>средний</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>минколумнсмедиум</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает минимальное число столбцов, которое <strong>инриббонгаллери</strong> отображается в макете группы <em>средних</em> , перед переключением на <em>малый</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>текстпоситион</strong><br/></td>
<td>текстпоситионтипе<br/></td>
<td>Нет<br/></td>
<td>Указывает, где отображается метка элемента относительно изображения. <br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> Нижний<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Ыть<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Слева<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Крывает<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Справа<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Лучшая<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Тип</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> Файлов<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Меню<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                           | Описание                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                                     | Может происходить один или несколько раз<br/> <br/> |
| [**Инриббонгаллери. Менуграупс**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Должно выполняться только один раз<br/> <br/>     |
| [**Инриббонгаллери. Менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |
| [**Переключатель**](windowsribbon-element-button.md)<br/>                                       | Может происходить один или несколько раз<br/> <br/> |
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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Куиккакцесстулбар. Аппликатиондефаултс</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 и более поздние версии.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md) или [**Group**](windowsribbon-element-group.md) .

На следующем снимке экрана показана лента в элементе управления " [Коллекция ленты](windowsribbon-controls-inribbongallery.md) " в Microsoft Paint для Windows 7.

![снимок экрана: элемент управления "Коллекция на ленте" на ленте Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [коллекции на ленте](windowsribbon-controls-inribbongallery.md).

В этом разделе кода показаны объявления команд **инриббонгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **инриббонгаллери** .


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



В этом разделе кода показаны объявления элементов управления **инриббонгаллери** .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Нет        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления "Коллекция ленты"](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

 

 






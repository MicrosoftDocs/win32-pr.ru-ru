---
title: Сплитбуттонгаллери, элемент
description: Представляет элемент управления коллекции разделенных кнопок с раскрывающимся меню на основе галереи.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- элемент сплитбуттонгаллери Windows лента
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c28c2f87a1d8fb165f02ad71c96b38bcbb381bb3590bd9bff98b3feb364044bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850830"
---
# <a name="splitbuttongallery-element"></a>Сплитбуттонгаллери, элемент

Представляет элемент управления [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md) с раскрывающимся меню на основе галереи.

## <a name="usage"></a>Использование

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
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
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>итемвидс</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Значение по умолчанию — -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>текстпоситион</strong><br/></td>
<td>текстпоситионтипе<br/></td>
<td>Нет<br/></td>
<td>Ограничено одним из следующих значений:<br/> <br/>
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



| Элемент                                                                                                 | Описание                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Кнопка**](windowsribbon-element-button.md)<br/>                                               | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                                           | Может происходить один или несколько раз<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Может происходить один или несколько раз<br/> <br/> |
| [**Сплитбуттонгаллери. Менуграупс**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Должно выполняться только один раз<br/> <br/>     |
| [**Сплитбуттонгаллери. Менулайаут**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Может происходить один или несколько раз<br/> <br/> |



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

Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md)или [**SplitButton**](windowsribbon-element-splitbutton.md) .

**Сплитбуттонгаллери** поддерживает [режимы приложений](ribbon-applicationmodes.md).

[Пользовательский интерфейс \_ PKEY \_ булеанвалуе](windowsribbon-reference-properties-uipkey-booleanvalue.md) используется приложением для запроса состояния переключения для элемента управления "Кнопка" в **сплитбуттонгаллери**.

на следующем снимке экрана показан элемент управления ["коллекция кнопок с разделением ленты"](windowsribbon-controls-splitbuttongallery.md) в Microsoft Paint для Windows 7.

![снимок экрана: элемент управления "коллекция разделенных кнопок" в Microsoft Paint для Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md).

В этом разделе кода показаны объявления команд **сплитбуттонгаллери** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **сплитбуттонгаллери** .


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



В этом разделе кода показаны объявления элементов управления **сплитбуттонгаллери** .


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a>Сведения об элементе


- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

 


---
title: Менуграуп, элемент
description: Представляет контейнер элементов управления, отображаемых в коллекции, меню или панели инструментов.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Лента Windows для элемента Менуграуп
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787483"
---
# <a name="menugroup-element"></a>Менуграуп, элемент

Представляет контейнер элементов управления, отображаемых в коллекции, меню или панели инструментов.

## <a name="usage"></a>Использование

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>Класс</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Задает размер и стиль макета для элементов в пользовательском интерфейсе меню.<br/> Ресурс изображения может быть представлен в двух размерах (крупный и маленький) и связан с элементом в разметке с помощью элементов свойств <a href="windowsribbon-element-command-largeimages.md"><strong>Command. ларжеимажес</strong></a> и <a href="windowsribbon-element-command-smallimages.md"><strong>Command. смаллимажес</strong></a> . Если предоставляется только один образ, платформа при необходимости изменяет ее размер.<br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Стандардитемс)<br/> </dt> <dd> По умолчанию. <br/> Стиль: небольшое изображение и невыделенный текст.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (Мажоритемс)<br/> </dt> <dd> Стиль: крупный рисунок и полужирный текст.<br/>
<blockquote>
[!Note]<br />
Если <strong>менуграуп</strong> является дочерним элементом <a href="windowsribbon-element-applicationmenu.md"><strong>Аппликатионмену</strong></a>, атрибут <em>класса</em> не учитывается и стиль <code>MajorItems</code> применяется платформой.
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
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
| [**Кнопка**](windowsribbon-element-button.md)<br/>                           | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Может происходить один или несколько раз<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>         | Может происходить один или несколько раз<br/> <br/> |
| [**фонтконтрол**](windowsribbon-element-fontcontrol.md)<br/>                 | Может выполняться не более одного раза<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Может происходить один или несколько раз<br/> <br/> |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>   | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**аппликатионмену**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**Дропдовнгаллери. Менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**Инриббонгаллери. Менуграупс**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**минитулбар**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton. Менуграупс**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**Сплитбуттонгаллери. Менуграупс**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Комментарии

Обязательный.

Должен быть хотя бы один раз для каждого элемента [**аппликатионмену**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)или [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .

Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, **менуграуп** ограничивается следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md).

Если [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнгаллери. менуграупс**](windowsribbon-element-dropdowngallery-menugroups.md), [**инриббонгаллери. менуграупс**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md)или [**сплитбуттонгаллери. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) является родительским элементом, **MenuGroup** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).

Если [**минитулбар**](windowsribbon-element-minitoolbar.md) является родительским элементом, **менуграуп** ограничен следующими дочерними элементами: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**фонтконтрол**](windowsribbon-element-fontcontrol.md) [**,,**](windowsribbon-element-spinner.md) [**SplitButton**](windowsribbon-element-splitbutton.md), [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)или [**ToggleButton**](windowsribbon-element-togglebutton.md).

Атрибут Class не требуется, если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом. Платформа применяет значение Мажоритемс для атрибута класса.

Если [**аппликатионмену**](windowsribbon-element-applicationmenu.md) является родительским элементом, атрибут Class не является обязательным.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом **менуграуп** .

В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с большим и небольшим ресурсом изображения. Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **менуграуп** с `StandardItems` и `MajorItems` .


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Нет        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Указание ресурсов изображения ленты](windowsribbon-imageformats.md)
</dt> <dt>

[Группа меню](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 






---
title: Элемент SplitButton
description: Представляет стандартный элемент управления "кнопка разворачивающейся кнопки".
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- элемент SplitButton Windows лента
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07bc97a3c75a16c1a11783a13514a8ab5b3478c6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622740"
---
# <a name="splitbutton-element"></a>Элемент SplitButton

Представляет стандартный элемент управления ["кнопка разворачивающейся кнопки"](windowsribbon-controls-splitbutton.md) .

## <a name="usage"></a>Использование

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
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



| Элемент                                                                                   | Описание                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Кнопка**](windowsribbon-element-button.md)<br/>                                 | Может происходить один или несколько раз<br/> <br/> |
| [**Установка**](windowsribbon-element-checkbox.md)<br/>                             | Может происходить один или несколько раз<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Может происходить один или несколько раз<br/> <br/> |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>               | Может происходить один или несколько раз<br/> <br/> |
| **SplitButton**<br/>                                                                | Может происходить один или несколько раз<br/> <br/> |
| [**SplitButton. Буттонитем**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |
| [**SplitButton. Менуграупс**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>         | Может происходить один или несколько раз<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>             |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Группа**](windowsribbon-element-group.md)<br/>                           |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), **SplitButton** или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

**SplitButton** поддерживает [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложения.

[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) и [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) не являются допустимыми дочерними элементами [**DropDownButton**](windowsribbon-element-dropdownbutton.md) , если **DropDownButton** является потомком [**аппликатионмену**](windowsribbon-element-applicationmenu.md).

[**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md) должен быть выполнен один раз, если следующие элементы отсутствуют в качестве дочерних элементов **SplitButton**:

-   [**Кнопка**](windowsribbon-element-button.md)
-   [**Установка**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md)
-   [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Эти элементы управления обрабатываются как дочерние элементы одного элемента по умолчанию [**SplitButton. менуграупс**](windowsribbon-element-splitbutton-menugroups.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [кнопки Split](windowsribbon-controls-splitbutton.md).

В этом разделе кода показаны объявления команд **SplitButton** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .


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



В этом разделе кода показаны объявления элемента управления **SplitButton** .


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

- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления "разворачивающаяся кнопка"](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


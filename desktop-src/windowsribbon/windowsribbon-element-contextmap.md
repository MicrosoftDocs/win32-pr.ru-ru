---
title: Контекстмап, элемент
description: Представляет сопоставление ContextMenu и Минитулбар пары.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Лента Windows для элемента Контекстмап
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754fc75ca09e39cdc7eabbeae2a0a2d2630c31f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443015"
---
# <a name="contextmap-element"></a>Контекстмап, элемент

Представляет сопоставление [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) пары.

## <a name="usage"></a>Использование

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
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
<td><strong>ContextMenu</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Должен соответствовать существующему имени <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em></em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>минитулбар</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Должен соответствовать существующему имени <a href="windowsribbon-element-minitoolbar.md"><strong>минитулбар</strong></a> <em></em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**Контекстпопуп. Контекстмапс**](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может происходить один или несколько раз для каждого [**контекстпопуп. контекстмапс**](windowsribbon-element-contextpopup-contextmaps.md).

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .

В этом разделе кода показан набор объявлений элементов управления **контекстмап** .


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>Сведения об элементе


* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Контекстное меню элемента управления](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






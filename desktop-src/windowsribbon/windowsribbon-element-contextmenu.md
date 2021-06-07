---
title: Элемент ContextMenu
description: Представляет элемент управления "контекстное меню".
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Лента Windows для элемента ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 916a031ed642a76fb22ecc58dbbe1ce29cbcd105
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443474"
---
# <a name="contextmenu-element"></a>Элемент ContextMenu

Представляет элемент управления "контекстное меню".

## <a name="usage"></a>Использование

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a>Атрибуты



| attribute           | Тип                 | Обязательно       | Описание                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Имя**<br/> | xs:string<br/> | Да<br/> | <dt> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                         | Описание                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Контекстпопуп. ContextMenu**](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может происходить один или несколько раз для каждого [**контекстпопуп. ContextMenu**](windowsribbon-element-contextpopup-contextmenus.md).

> [!IMPORTANT]
> **ContextMenu** не может размещать [поле со списком](windowsribbon-controls-combobox.md) или элементы управления " [Счетчик](windowsribbon-controls-spinner.md) ".

 

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .

В этом разделе кода показан набор объявлений элементов управления **ContextMenu** .


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
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Контекстное меню элемента управления](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






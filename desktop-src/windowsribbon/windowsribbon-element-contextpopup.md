---
title: Контекстпопуп, элемент
description: Представляет всплывающий элемент управления "контекст" в представлении Контекстпопуп.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- элемент контекстпопуп Windows лента
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8fddda30a765eb314c7a29934c9fcdd12404647de9f1e480275f8fa685b50827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840794"
---
# <a name="contextpopup-element"></a>Контекстпопуп, элемент

Представляет [всплывающий элемент управления "контекст"](windowsribbon-controls-contextpopup.md) в представлении контекстпопуп.

## <a name="usage"></a>Использование

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                         | Описание                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Контекстпопуп. Контекстмапс**](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | Может выполняться не более одного раза<br/> <br/> |
| [**Контекстпопуп. ContextMenu**](windowsribbon-element-contextpopup-contextmenus.md)<br/> | Может выполняться не более одного раза<br/> <br/> |
| [**Контекстпопуп. Минитулбарс**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого [**приложения. views**](windowsribbon-element-application-views.md).

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для представления **контекстпопуп** .


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

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Контекстное меню элемента управления](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






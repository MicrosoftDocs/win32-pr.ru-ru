---
title: Контекстпопуп, элемент
description: Представляет всплывающий элемент управления "контекст" в представлении Контекстпопуп.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Лента Windows для элемента Контекстпопуп
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f779b0196d14fb42246c2a10d476352d835b6cf8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443471"
---
# <a name="contextpopup-element"></a><span data-ttu-id="490ef-104">Контекстпопуп, элемент</span><span class="sxs-lookup"><span data-stu-id="490ef-104">ContextPopup element</span></span>

<span data-ttu-id="490ef-105">Представляет [всплывающий элемент управления "контекст"](windowsribbon-controls-contextpopup.md) в представлении контекстпопуп.</span><span class="sxs-lookup"><span data-stu-id="490ef-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="490ef-106">Использование</span><span class="sxs-lookup"><span data-stu-id="490ef-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="490ef-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="490ef-107">Attributes</span></span>

<span data-ttu-id="490ef-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="490ef-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="490ef-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="490ef-109">Child elements</span></span>



| <span data-ttu-id="490ef-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="490ef-110">Element</span></span>                                                                                         | <span data-ttu-id="490ef-111">Описание</span><span class="sxs-lookup"><span data-stu-id="490ef-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="490ef-112">**Контекстпопуп. Контекстмапс**</span><span class="sxs-lookup"><span data-stu-id="490ef-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="490ef-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="490ef-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="490ef-114">**Контекстпопуп. ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="490ef-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="490ef-115">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="490ef-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="490ef-116">**Контекстпопуп. Минитулбарс**</span><span class="sxs-lookup"><span data-stu-id="490ef-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="490ef-117">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="490ef-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="490ef-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="490ef-118">Parent elements</span></span>



| <span data-ttu-id="490ef-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="490ef-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="490ef-120">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="490ef-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="490ef-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="490ef-121">Remarks</span></span>

<span data-ttu-id="490ef-122">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="490ef-122">Optional.</span></span>

<span data-ttu-id="490ef-123">Может встречаться не более одного раза для каждого [**приложения. views**](windowsribbon-element-application-views.md).</span><span class="sxs-lookup"><span data-stu-id="490ef-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="490ef-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="490ef-124">Examples</span></span>

<span data-ttu-id="490ef-125">В следующем примере показана базовая разметка для представления **контекстпопуп** .</span><span class="sxs-lookup"><span data-stu-id="490ef-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="490ef-126">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="490ef-126">Element information</span></span>

* <span data-ttu-id="490ef-127">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="490ef-127">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="490ef-128">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="490ef-128">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="490ef-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="490ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490ef-130">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="490ef-130">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






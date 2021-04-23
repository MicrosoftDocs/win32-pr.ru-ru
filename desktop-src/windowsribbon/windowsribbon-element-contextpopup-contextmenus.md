---
title: Контекстпопуп. ContextMenus, свойство
description: Представляет контейнер для элементов ContextMenu.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- Лента Windows для свойства Контекстпопуп. ContextMenu
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701075"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="1d596-104">Контекстпопуп. ContextMenus, свойство</span><span class="sxs-lookup"><span data-stu-id="1d596-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="1d596-105">Представляет контейнер для элементов [**ContextMenu**](windowsribbon-element-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="1d596-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="1d596-106">Использование</span><span class="sxs-lookup"><span data-stu-id="1d596-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="1d596-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d596-107">Attributes</span></span>

<span data-ttu-id="1d596-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1d596-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1d596-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1d596-109">Child elements</span></span>



| <span data-ttu-id="1d596-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d596-110">Element</span></span>                                                             | <span data-ttu-id="1d596-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1d596-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="1d596-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="1d596-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="1d596-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="1d596-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1d596-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1d596-114">Parent elements</span></span>



| <span data-ttu-id="1d596-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d596-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="1d596-116">**контекстпопуп**</span><span class="sxs-lookup"><span data-stu-id="1d596-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1d596-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d596-117">Remarks</span></span>

<span data-ttu-id="1d596-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1d596-118">Optional.</span></span>

<span data-ttu-id="1d596-119">Может встречаться не более одного раза для каждого [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="1d596-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1d596-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="1d596-120">Examples</span></span>

<span data-ttu-id="1d596-121">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="1d596-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="1d596-122">В этом разделе кода показано объявление элемента управления **контекстпопуп. ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="1d596-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1d596-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1d596-123">Requirements</span></span>



| <span data-ttu-id="1d596-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1d596-124">Requirement</span></span> | <span data-ttu-id="1d596-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1d596-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1d596-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d596-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1d596-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1d596-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1d596-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d596-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1d596-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d596-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d596-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d596-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d596-131">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="1d596-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






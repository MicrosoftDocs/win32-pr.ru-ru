---
title: Контекстпопуп. Контекстмапс, свойство
description: Представляет контейнер для элементов Контекстмап.
ms.assetid: 06dfd4ba-a1d8-48bb-b185-d265e007a820
keywords:
- Лента Windows для свойства Контекстпопуп. Контекстмапс
topic_type:
- apiref
api_name:
- ContextPopup.ContextMaps
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034381c4af840219ff1d6dd4d7a73aa34f528915
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701074"
---
# <a name="contextpopupcontextmaps-property"></a><span data-ttu-id="7b21f-104">Контекстпопуп. Контекстмапс, свойство</span><span class="sxs-lookup"><span data-stu-id="7b21f-104">ContextPopup.ContextMaps property</span></span>

<span data-ttu-id="7b21f-105">Представляет контейнер для элементов [**контекстмап**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="7b21f-105">Represents a container for [**ContextMap**](windowsribbon-element-contextmap.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="7b21f-106">Использование</span><span class="sxs-lookup"><span data-stu-id="7b21f-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMaps>
  child elements
</ContextPopup.ContextMaps>
```

## <a name="attributes"></a><span data-ttu-id="7b21f-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b21f-107">Attributes</span></span>

<span data-ttu-id="7b21f-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="7b21f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7b21f-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7b21f-109">Child elements</span></span>



| <span data-ttu-id="7b21f-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="7b21f-110">Element</span></span>                                                           | <span data-ttu-id="7b21f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7b21f-111">Description</span></span>                                        |
|-------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7b21f-112">**контекстмап**</span><span class="sxs-lookup"><span data-stu-id="7b21f-112">**ContextMap**</span></span>](windowsribbon-element-contextmap.md)<br/> | <span data-ttu-id="7b21f-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="7b21f-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7b21f-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7b21f-114">Parent elements</span></span>



| <span data-ttu-id="7b21f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="7b21f-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="7b21f-116">**контекстпопуп**</span><span class="sxs-lookup"><span data-stu-id="7b21f-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7b21f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b21f-117">Remarks</span></span>

<span data-ttu-id="7b21f-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7b21f-118">Optional.</span></span>

<span data-ttu-id="7b21f-119">Может встречаться не более одного раза для каждого [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="7b21f-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7b21f-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="7b21f-120">Examples</span></span>

<span data-ttu-id="7b21f-121">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="7b21f-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="7b21f-122">В этом разделе кода показано объявление элемента управления **контекстпопуп. контекстмапс** .</span><span class="sxs-lookup"><span data-stu-id="7b21f-122">This section of code shows a **ContextPopup.ContextMaps** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7b21f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7b21f-123">Requirements</span></span>



| <span data-ttu-id="7b21f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7b21f-124">Requirement</span></span> | <span data-ttu-id="7b21f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7b21f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7b21f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b21f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7b21f-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7b21f-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7b21f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b21f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7b21f-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b21f-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b21f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b21f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b21f-131">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="7b21f-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






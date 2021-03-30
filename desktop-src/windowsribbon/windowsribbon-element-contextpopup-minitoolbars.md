---
title: Контекстпопуп. Минитулбарс, свойство
description: Представляет контейнер для элементов Минитулбар.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Лента Windows для свойства Контекстпопуп. Минитулбарс
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492501"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="8edc7-104">Контекстпопуп. Минитулбарс, свойство</span><span class="sxs-lookup"><span data-stu-id="8edc7-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="8edc7-105">Представляет контейнер для элементов [**минитулбар**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="8edc7-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="8edc7-106">Использование</span><span class="sxs-lookup"><span data-stu-id="8edc7-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="8edc7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8edc7-107">Attributes</span></span>

<span data-ttu-id="8edc7-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="8edc7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8edc7-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8edc7-109">Child elements</span></span>



| <span data-ttu-id="8edc7-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="8edc7-110">Element</span></span>                                                             | <span data-ttu-id="8edc7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8edc7-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8edc7-112">**минитулбар**</span><span class="sxs-lookup"><span data-stu-id="8edc7-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="8edc7-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="8edc7-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8edc7-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8edc7-114">Parent elements</span></span>



| <span data-ttu-id="8edc7-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="8edc7-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="8edc7-116">**контекстпопуп**</span><span class="sxs-lookup"><span data-stu-id="8edc7-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8edc7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8edc7-117">Remarks</span></span>

<span data-ttu-id="8edc7-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="8edc7-118">Optional.</span></span>

<span data-ttu-id="8edc7-119">Может встречаться не более одного раза для каждого [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="8edc7-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="8edc7-120">Так как элементы управления в [**минитулбар**](windowsribbon-element-minitoolbar.md) недоступны для клавиатуры, команды, которые они предоставляют, должны быть доступны в любом расположении ленты.</span><span class="sxs-lookup"><span data-stu-id="8edc7-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="8edc7-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="8edc7-121">Examples</span></span>

<span data-ttu-id="8edc7-122">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="8edc7-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="8edc7-123">В этом разделе кода показано объявление элемента управления **контекстпопуп. минитулбарс** .</span><span class="sxs-lookup"><span data-stu-id="8edc7-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8edc7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8edc7-124">Requirements</span></span>



| <span data-ttu-id="8edc7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8edc7-125">Requirement</span></span> | <span data-ttu-id="8edc7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8edc7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8edc7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8edc7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8edc7-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8edc7-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8edc7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8edc7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8edc7-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8edc7-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8edc7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8edc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edc7-132">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="8edc7-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






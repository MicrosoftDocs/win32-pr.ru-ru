---
title: Минитулбар, элемент
description: Представляет контекстную панель инструментов.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Лента Windows для элемента Минитулбар
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443265"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="42751-104">Минитулбар, элемент</span><span class="sxs-lookup"><span data-stu-id="42751-104">MiniToolbar element</span></span>

<span data-ttu-id="42751-105">Представляет контекстную панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="42751-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="42751-106">Использование</span><span class="sxs-lookup"><span data-stu-id="42751-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="42751-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="42751-107">Attributes</span></span>



| <span data-ttu-id="42751-108">attribute</span><span class="sxs-lookup"><span data-stu-id="42751-108">Attribute</span></span>           | <span data-ttu-id="42751-109">Тип</span><span class="sxs-lookup"><span data-stu-id="42751-109">Type</span></span>                 | <span data-ttu-id="42751-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="42751-110">Required</span></span>       | <span data-ttu-id="42751-111">Описание</span><span class="sxs-lookup"><span data-stu-id="42751-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42751-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="42751-112">**Name**</span></span><br/> | <span data-ttu-id="42751-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="42751-113">xs:string</span></span><br/> | <span data-ttu-id="42751-114">Да</span><span class="sxs-lookup"><span data-stu-id="42751-114">Yes</span></span><br/> | <span data-ttu-id="42751-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="42751-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="42751-116">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="42751-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="42751-117">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="42751-117">Child elements</span></span>



| <span data-ttu-id="42751-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="42751-118">Element</span></span>                                                         | <span data-ttu-id="42751-119">Описание</span><span class="sxs-lookup"><span data-stu-id="42751-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="42751-120">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="42751-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="42751-121">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="42751-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="42751-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="42751-122">Parent elements</span></span>



| <span data-ttu-id="42751-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="42751-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42751-124">**Контекстпопуп. Минитулбарс**</span><span class="sxs-lookup"><span data-stu-id="42751-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="42751-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="42751-125">Remarks</span></span>

<span data-ttu-id="42751-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="42751-126">Optional.</span></span>

<span data-ttu-id="42751-127">Может происходить один или несколько раз для каждого [**контекстпопуп. минитулбарс**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="42751-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="42751-128">В отличие от элемента [**ContextMenu**](windowsribbon-element-contextmenu.md) , **минитулбар** остается видимым при щелчке элемента на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="42751-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="42751-129">При отображении без [**ContextMenu**](windowsribbon-element-contextmenu.md) **минитулбар** исчезает при перемещении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="42751-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="42751-130">Из-за этого поведения [**ContextMenu**](windowsribbon-element-contextmenu.md) должен отображаться в близком к указателю мыши.</span><span class="sxs-lookup"><span data-stu-id="42751-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="42751-131">Так как элементы управления в **минитулбар** недоступны для клавиатуры, команды, которые они предоставляют, должны быть доступны в любом расположении ленты.</span><span class="sxs-lookup"><span data-stu-id="42751-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="42751-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="42751-132">Examples</span></span>

<span data-ttu-id="42751-133">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="42751-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="42751-134">В этом разделе кода показан набор объявлений элементов управления **минитулбар** .</span><span class="sxs-lookup"><span data-stu-id="42751-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="42751-135">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="42751-135">Element information</span></span>

* <span data-ttu-id="42751-136">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="42751-136">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="42751-137">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="42751-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="42751-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42751-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42751-139">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="42751-139">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






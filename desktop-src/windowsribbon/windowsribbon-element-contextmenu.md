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
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783915"
---
# <a name="contextmenu-element"></a><span data-ttu-id="b06f2-104">Элемент ContextMenu</span><span class="sxs-lookup"><span data-stu-id="b06f2-104">ContextMenu element</span></span>

<span data-ttu-id="b06f2-105">Представляет элемент управления "контекстное меню".</span><span class="sxs-lookup"><span data-stu-id="b06f2-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="b06f2-106">Использование</span><span class="sxs-lookup"><span data-stu-id="b06f2-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="b06f2-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b06f2-107">Attributes</span></span>



| <span data-ttu-id="b06f2-108">attribute</span><span class="sxs-lookup"><span data-stu-id="b06f2-108">Attribute</span></span>           | <span data-ttu-id="b06f2-109">Тип</span><span class="sxs-lookup"><span data-stu-id="b06f2-109">Type</span></span>                 | <span data-ttu-id="b06f2-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="b06f2-110">Required</span></span>       | <span data-ttu-id="b06f2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b06f2-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b06f2-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="b06f2-112">**Name**</span></span><br/> | <span data-ttu-id="b06f2-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b06f2-113">xs:string</span></span><br/> | <span data-ttu-id="b06f2-114">Да</span><span class="sxs-lookup"><span data-stu-id="b06f2-114">Yes</span></span><br/> | <span data-ttu-id="b06f2-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b06f2-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b06f2-116">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="b06f2-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="b06f2-117">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b06f2-117">Child elements</span></span>



| <span data-ttu-id="b06f2-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="b06f2-118">Element</span></span>                                                         | <span data-ttu-id="b06f2-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b06f2-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="b06f2-120">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="b06f2-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="b06f2-121">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="b06f2-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b06f2-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b06f2-122">Parent elements</span></span>



| <span data-ttu-id="b06f2-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="b06f2-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b06f2-124">**Контекстпопуп. ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="b06f2-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b06f2-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b06f2-125">Remarks</span></span>

<span data-ttu-id="b06f2-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b06f2-126">Optional.</span></span>

<span data-ttu-id="b06f2-127">Может происходить один или несколько раз для каждого [**контекстпопуп. ContextMenu**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="b06f2-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b06f2-128">**ContextMenu** не может размещать [поле со списком](windowsribbon-controls-combobox.md) или элементы управления " [Счетчик](windowsribbon-controls-spinner.md) ".</span><span class="sxs-lookup"><span data-stu-id="b06f2-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b06f2-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="b06f2-129">Examples</span></span>

<span data-ttu-id="b06f2-130">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="b06f2-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="b06f2-131">В этом разделе кода показан набор объявлений элементов управления **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="b06f2-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="b06f2-132">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b06f2-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b06f2-133">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="b06f2-133">Minimum supported system</span></span><br/> | <span data-ttu-id="b06f2-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b06f2-134">Windows 7</span></span> |
| <span data-ttu-id="b06f2-135">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="b06f2-135">Can be empty</span></span>                        | <span data-ttu-id="b06f2-136">Нет</span><span class="sxs-lookup"><span data-stu-id="b06f2-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="b06f2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b06f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06f2-138">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="b06f2-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






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
# <a name="contextmap-element"></a><span data-ttu-id="e5976-104">Контекстмап, элемент</span><span class="sxs-lookup"><span data-stu-id="e5976-104">ContextMap element</span></span>

<span data-ttu-id="e5976-105">Представляет сопоставление [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) пары.</span><span class="sxs-lookup"><span data-stu-id="e5976-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="e5976-106">Использование</span><span class="sxs-lookup"><span data-stu-id="e5976-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="e5976-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5976-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5976-108">attribute</span><span class="sxs-lookup"><span data-stu-id="e5976-108">Attribute</span></span></th>
<th><span data-ttu-id="e5976-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e5976-109">Type</span></span></th>
<th><span data-ttu-id="e5976-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e5976-110">Required</span></span></th>
<th><span data-ttu-id="e5976-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e5976-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5976-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="e5976-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="e5976-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="e5976-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e5976-114">Нет</span><span class="sxs-lookup"><span data-stu-id="e5976-114">No</span></span><br/></td>
<td><span data-ttu-id="e5976-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e5976-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="e5976-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="e5976-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e5976-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="e5976-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="e5976-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="e5976-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e5976-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="e5976-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5976-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="e5976-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="e5976-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e5976-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="e5976-122">Нет</span><span class="sxs-lookup"><span data-stu-id="e5976-122">No</span></span><br/></td>
<td><span data-ttu-id="e5976-123">Должен соответствовать существующему имени <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em></em>.</span><span class="sxs-lookup"><span data-stu-id="e5976-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="e5976-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e5976-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e5976-125">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="e5976-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5976-126"><strong>минитулбар</strong></span><span class="sxs-lookup"><span data-stu-id="e5976-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="e5976-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="e5976-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="e5976-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e5976-128">No</span></span><br/></td>
<td><span data-ttu-id="e5976-129">Должен соответствовать существующему имени <a href="windowsribbon-element-minitoolbar.md"><strong>минитулбар</strong></a> <em></em>.</span><span class="sxs-lookup"><span data-stu-id="e5976-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="e5976-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e5976-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e5976-131">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="e5976-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e5976-132">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e5976-132">Child elements</span></span>

<span data-ttu-id="e5976-133">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="e5976-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e5976-134">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e5976-134">Parent elements</span></span>



| <span data-ttu-id="e5976-135">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5976-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5976-136">**Контекстпопуп. Контекстмапс**</span><span class="sxs-lookup"><span data-stu-id="e5976-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e5976-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5976-137">Remarks</span></span>

<span data-ttu-id="e5976-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e5976-138">Optional.</span></span>

<span data-ttu-id="e5976-139">Может происходить один или несколько раз для каждого [**контекстпопуп. контекстмапс**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="e5976-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e5976-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="e5976-140">Examples</span></span>

<span data-ttu-id="e5976-141">В следующем примере показана базовая разметка для представления [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="e5976-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="e5976-142">В этом разделе кода показан набор объявлений элементов управления **контекстмап** .</span><span class="sxs-lookup"><span data-stu-id="e5976-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e5976-143">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e5976-143">Element information</span></span>


* <span data-ttu-id="e5976-144">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5976-144">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e5976-145">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="e5976-145">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="e5976-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5976-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5976-147">Контекстное меню элемента управления</span><span class="sxs-lookup"><span data-stu-id="e5976-147">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






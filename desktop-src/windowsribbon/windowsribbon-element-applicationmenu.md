---
title: Аппликатионмену, элемент
description: Представляет меню приложения. | Аппликатионмену, элемент
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Лента Windows для элемента Аппликатионмену
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a02193b4c3e61b4b8cf2f129619969f6a82a84ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273542"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="ad17c-105">Аппликатионмену, элемент</span><span class="sxs-lookup"><span data-stu-id="ad17c-105">ApplicationMenu element</span></span>

<span data-ttu-id="ad17c-106">Представляет [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="ad17c-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ad17c-107">Использование</span><span class="sxs-lookup"><span data-stu-id="ad17c-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="ad17c-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad17c-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad17c-109">attribute</span><span class="sxs-lookup"><span data-stu-id="ad17c-109">Attribute</span></span></th>
<th><span data-ttu-id="ad17c-110">Тип</span><span class="sxs-lookup"><span data-stu-id="ad17c-110">Type</span></span></th>
<th><span data-ttu-id="ad17c-111">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ad17c-111">Required</span></span></th>
<th><span data-ttu-id="ad17c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ad17c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad17c-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ad17c-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ad17c-114">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="ad17c-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ad17c-115">Нет</span><span class="sxs-lookup"><span data-stu-id="ad17c-115">No</span></span><br/></td>
<td><span data-ttu-id="ad17c-116">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ad17c-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ad17c-117">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="ad17c-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ad17c-118">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="ad17c-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ad17c-119">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="ad17c-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ad17c-120">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="ad17c-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ad17c-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ad17c-121">Child elements</span></span>



| <span data-ttu-id="ad17c-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="ad17c-122">Element</span></span>                                                                                             | <span data-ttu-id="ad17c-123">Описание</span><span class="sxs-lookup"><span data-stu-id="ad17c-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ad17c-124">**Аппликатионмену. Рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="ad17c-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="ad17c-125">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="ad17c-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="ad17c-126">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="ad17c-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="ad17c-127">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="ad17c-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ad17c-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ad17c-128">Parent elements</span></span>



| <span data-ttu-id="ad17c-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="ad17c-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad17c-130">**Лента. Аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="ad17c-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ad17c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad17c-131">Remarks</span></span>

<span data-ttu-id="ad17c-132">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ad17c-132">Required.</span></span>

<span data-ttu-id="ad17c-133">Должен выполняться ровно один раз для каждой [**ленты. аппликатионмену**](windowsribbon-element-ribbon-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="ad17c-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="ad17c-134">Дочерние элементы элемента **аппликатионмену** должны находиться в указанном порядке:</span><span class="sxs-lookup"><span data-stu-id="ad17c-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="ad17c-135">**Аппликатионмену. Рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="ad17c-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="ad17c-136">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="ad17c-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="ad17c-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="ad17c-137">Examples</span></span>

<span data-ttu-id="ad17c-138">В следующем примере показана базовая разметка для [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="ad17c-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="ad17c-139">В этом разделе кода показаны объявления команд **аппликатионмену** .</span><span class="sxs-lookup"><span data-stu-id="ad17c-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="ad17c-140">В этом разделе кода показаны объявления элементов управления **аппликатионмену** .</span><span class="sxs-lookup"><span data-stu-id="ad17c-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="ad17c-141">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ad17c-141">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ad17c-142">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="ad17c-142">Minimum supported system</span></span><br/> | <span data-ttu-id="ad17c-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad17c-143">Windows 7</span></span> |
| <span data-ttu-id="ad17c-144">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ad17c-144">Can be empty</span></span>                        | <span data-ttu-id="ad17c-145">Нет</span><span class="sxs-lookup"><span data-stu-id="ad17c-145">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ad17c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad17c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad17c-147">Элемент управления меню приложения</span><span class="sxs-lookup"><span data-stu-id="ad17c-147">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 






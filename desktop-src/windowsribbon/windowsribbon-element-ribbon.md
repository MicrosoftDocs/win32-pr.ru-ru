---
title: Элемент Ribbon
description: Представляет элемент управления ленты в представлении ленты.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Лента ленты Windows для элемента ленты
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445005"
---
# <a name="ribbon-element"></a><span data-ttu-id="45d8b-104">Элемент Ribbon</span><span class="sxs-lookup"><span data-stu-id="45d8b-104">Ribbon element</span></span>

<span data-ttu-id="45d8b-105">Представляет элемент управления ленты в представлении ленты.</span><span class="sxs-lookup"><span data-stu-id="45d8b-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="45d8b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="45d8b-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="45d8b-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="45d8b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45d8b-108">attribute</span><span class="sxs-lookup"><span data-stu-id="45d8b-108">Attribute</span></span></th>
<th><span data-ttu-id="45d8b-109">Тип</span><span class="sxs-lookup"><span data-stu-id="45d8b-109">Type</span></span></th>
<th><span data-ttu-id="45d8b-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="45d8b-110">Required</span></span></th>
<th><span data-ttu-id="45d8b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="45d8b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45d8b-112"><strong>граупспаЦинг</strong></span><span class="sxs-lookup"><span data-stu-id="45d8b-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="45d8b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="45d8b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="45d8b-114">Нет</span><span class="sxs-lookup"><span data-stu-id="45d8b-114">No</span></span><br/></td>
<td><span data-ttu-id="45d8b-115"><dt><span></span><span></span><strong></strong> Значительные</span><span class="sxs-lookup"><span data-stu-id="45d8b-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="45d8b-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45d8b-116">Default.</span></span> <br/> </dd> <span data-ttu-id="45d8b-117"><dt><span></span><span></span><strong></strong> Высокое</span><span class="sxs-lookup"><span data-stu-id="45d8b-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="45d8b-118"><dt><span></span><span></span><strong></strong> Достаточ</span><span class="sxs-lookup"><span data-stu-id="45d8b-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45d8b-119"><strong>Имя</strong></span><span class="sxs-lookup"><span data-stu-id="45d8b-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="45d8b-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="45d8b-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="45d8b-121">Нет</span><span class="sxs-lookup"><span data-stu-id="45d8b-121">No</span></span><br/></td>
<td><span data-ttu-id="45d8b-122">Используется для добавления аннотации в элемент Command.</span><span class="sxs-lookup"><span data-stu-id="45d8b-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="45d8b-123">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="45d8b-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="45d8b-124">Любая последовательность из нуля или более символов.</span><span class="sxs-lookup"><span data-stu-id="45d8b-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="45d8b-125">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="45d8b-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="45d8b-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="45d8b-126">Child elements</span></span>



| <span data-ttu-id="45d8b-127">Элемент</span><span class="sxs-lookup"><span data-stu-id="45d8b-127">Element</span></span>                                                                                         | <span data-ttu-id="45d8b-128">Описание</span><span class="sxs-lookup"><span data-stu-id="45d8b-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="45d8b-129">**Лента. Аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="45d8b-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="45d8b-130">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="45d8b-131">**Лента. Контекстуалтабс**</span><span class="sxs-lookup"><span data-stu-id="45d8b-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="45d8b-132">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="45d8b-133">**Лента. Хелпбуттон**</span><span class="sxs-lookup"><span data-stu-id="45d8b-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="45d8b-134">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="45d8b-135">**Лента. Куиккакцесстулбар**</span><span class="sxs-lookup"><span data-stu-id="45d8b-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="45d8b-136">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="45d8b-137">**Лента. Сизедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="45d8b-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="45d8b-138">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="45d8b-139">**Лента. вкладки**</span><span class="sxs-lookup"><span data-stu-id="45d8b-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="45d8b-140">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="45d8b-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="45d8b-141">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="45d8b-141">Parent elements</span></span>



| <span data-ttu-id="45d8b-142">Элемент</span><span class="sxs-lookup"><span data-stu-id="45d8b-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="45d8b-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="45d8b-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="45d8b-144">Remarks</span><span class="sxs-lookup"><span data-stu-id="45d8b-144">Remarks</span></span>

<span data-ttu-id="45d8b-145">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="45d8b-145">Required.</span></span>

<span data-ttu-id="45d8b-146">Должен выполняться только один раз для каждого элемента [**Application. views**](windowsribbon-element-application-views.md) .</span><span class="sxs-lookup"><span data-stu-id="45d8b-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="45d8b-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="45d8b-147">Examples</span></span>

<span data-ttu-id="45d8b-148">В следующем примере показана базовая разметка для представления **ленты** .</span><span class="sxs-lookup"><span data-stu-id="45d8b-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="45d8b-149">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="45d8b-149">Element information</span></span>




* <span data-ttu-id="45d8b-150">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="45d8b-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="45d8b-151">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="45d8b-151">**Can be empty**: No</span></span>



 

 






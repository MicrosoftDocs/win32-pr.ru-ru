---
title: Рецентитемс, элемент
description: Представляет элемент управления "Недавние элементы" в меню "приложение".
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Лента Windows для элемента Рецентитемс
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444115"
---
# <a name="recentitems-element"></a><span data-ttu-id="9f52c-104">Рецентитемс, элемент</span><span class="sxs-lookup"><span data-stu-id="9f52c-104">RecentItems element</span></span>

<span data-ttu-id="9f52c-105">Представляет элемент управления " [недавние элементы](windowsribbon-controls-recentitems.md) " в [меню "приложение](windowsribbon-controls-applicationmenu.md)".</span><span class="sxs-lookup"><span data-stu-id="9f52c-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="9f52c-106">Использование</span><span class="sxs-lookup"><span data-stu-id="9f52c-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="9f52c-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9f52c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f52c-108">attribute</span><span class="sxs-lookup"><span data-stu-id="9f52c-108">Attribute</span></span></th>
<th><span data-ttu-id="9f52c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="9f52c-109">Type</span></span></th>
<th><span data-ttu-id="9f52c-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9f52c-110">Required</span></span></th>
<th><span data-ttu-id="9f52c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9f52c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f52c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="9f52c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="9f52c-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="9f52c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="9f52c-114">Нет</span><span class="sxs-lookup"><span data-stu-id="9f52c-114">No</span></span><br/></td>
<td><span data-ttu-id="9f52c-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f52c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="9f52c-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="9f52c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9f52c-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="9f52c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="9f52c-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="9f52c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="9f52c-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="9f52c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f52c-120"><strong>енаблепиннинг</strong></span><span class="sxs-lookup"><span data-stu-id="9f52c-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="9f52c-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="9f52c-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="9f52c-122">Нет</span><span class="sxs-lookup"><span data-stu-id="9f52c-122">No</span></span><br/></td>
<td><span data-ttu-id="9f52c-123">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="9f52c-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="9f52c-124">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="9f52c-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9f52c-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f52c-125">Default.</span></span> <br/> </dd> <span data-ttu-id="9f52c-126"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="9f52c-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f52c-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="9f52c-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="9f52c-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="9f52c-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="9f52c-129">Нет</span><span class="sxs-lookup"><span data-stu-id="9f52c-129">No</span></span><br/></td>
<td><span data-ttu-id="9f52c-130">Число недавно отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="9f52c-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="9f52c-131">
<dt><span></span><span></span><strong></strong> (xs: nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="9f52c-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="9f52c-132">Целочисленное значение 0 или выше.</span><span class="sxs-lookup"><span data-stu-id="9f52c-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="9f52c-133">Значение по умолчанию — <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f52c-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9f52c-134">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9f52c-134">Child elements</span></span>

<span data-ttu-id="9f52c-135">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="9f52c-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9f52c-136">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9f52c-136">Parent elements</span></span>



| <span data-ttu-id="9f52c-137">Элемент</span><span class="sxs-lookup"><span data-stu-id="9f52c-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f52c-138">**Аппликатионмену. Рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="9f52c-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9f52c-139">Remarks</span><span class="sxs-lookup"><span data-stu-id="9f52c-139">Remarks</span></span>

<span data-ttu-id="9f52c-140">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9f52c-140">Required.</span></span>

<span data-ttu-id="9f52c-141">Должен выполняться ровно один раз для каждого элемента [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="9f52c-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="9f52c-142">Элемент управления [недавние элементы](windowsribbon-controls-recentitems.md) отображает список недавно использовавшихся элементов приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="9f52c-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="9f52c-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="9f52c-143">Examples</span></span>

<span data-ttu-id="9f52c-144">В следующем примере показана базовая разметка для элемента управления [недавние элементы](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="9f52c-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="9f52c-145">В следующем примере показано объявление команды **рецентитемс** .</span><span class="sxs-lookup"><span data-stu-id="9f52c-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="9f52c-146">В следующем примере показано связанное объявление элементов управления **рецентитемс** .</span><span class="sxs-lookup"><span data-stu-id="9f52c-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="9f52c-147">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9f52c-147">Element information</span></span>

* <span data-ttu-id="9f52c-148">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f52c-148">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="9f52c-149">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="9f52c-149">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="9f52c-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f52c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f52c-151">Элемент управления меню приложения</span><span class="sxs-lookup"><span data-stu-id="9f52c-151">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="9f52c-152">Элемент управления "Недавние элементы"</span><span class="sxs-lookup"><span data-stu-id="9f52c-152">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 






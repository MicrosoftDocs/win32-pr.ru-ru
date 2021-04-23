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
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104069511"
---
# <a name="recentitems-element"></a><span data-ttu-id="959b5-104">Рецентитемс, элемент</span><span class="sxs-lookup"><span data-stu-id="959b5-104">RecentItems element</span></span>

<span data-ttu-id="959b5-105">Представляет элемент управления " [недавние элементы](windowsribbon-controls-recentitems.md) " в [меню "приложение](windowsribbon-controls-applicationmenu.md)".</span><span class="sxs-lookup"><span data-stu-id="959b5-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="959b5-106">Использование</span><span class="sxs-lookup"><span data-stu-id="959b5-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="959b5-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="959b5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="959b5-108">attribute</span><span class="sxs-lookup"><span data-stu-id="959b5-108">Attribute</span></span></th>
<th><span data-ttu-id="959b5-109">Тип</span><span class="sxs-lookup"><span data-stu-id="959b5-109">Type</span></span></th>
<th><span data-ttu-id="959b5-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="959b5-110">Required</span></span></th>
<th><span data-ttu-id="959b5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="959b5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="959b5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="959b5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="959b5-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="959b5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="959b5-114">Нет</span><span class="sxs-lookup"><span data-stu-id="959b5-114">No</span></span><br/></td>
<td><span data-ttu-id="959b5-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="959b5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="959b5-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="959b5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="959b5-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="959b5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="959b5-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="959b5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="959b5-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="959b5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="959b5-120"><strong>енаблепиннинг</strong></span><span class="sxs-lookup"><span data-stu-id="959b5-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="959b5-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="959b5-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="959b5-122">Нет</span><span class="sxs-lookup"><span data-stu-id="959b5-122">No</span></span><br/></td>
<td><span data-ttu-id="959b5-123">Ограничение на одно из следующих значений (0 и 1 недопустимы):</span><span class="sxs-lookup"><span data-stu-id="959b5-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="959b5-124">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="959b5-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="959b5-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="959b5-125">Default.</span></span> <br/> </dd> <span data-ttu-id="959b5-126"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="959b5-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="959b5-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="959b5-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="959b5-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="959b5-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="959b5-129">Нет</span><span class="sxs-lookup"><span data-stu-id="959b5-129">No</span></span><br/></td>
<td><span data-ttu-id="959b5-130">Число недавно отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="959b5-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="959b5-131">
<dt><span></span><span></span><strong></strong> (xs: nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="959b5-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="959b5-132">Целочисленное значение 0 или выше.</span><span class="sxs-lookup"><span data-stu-id="959b5-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="959b5-133">Значение по умолчанию — <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="959b5-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="959b5-134">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="959b5-134">Child elements</span></span>

<span data-ttu-id="959b5-135">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="959b5-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="959b5-136">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="959b5-136">Parent elements</span></span>



| <span data-ttu-id="959b5-137">Элемент</span><span class="sxs-lookup"><span data-stu-id="959b5-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="959b5-138">**Аппликатионмену. Рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="959b5-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="959b5-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="959b5-139">Remarks</span></span>

<span data-ttu-id="959b5-140">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="959b5-140">Required.</span></span>

<span data-ttu-id="959b5-141">Должен выполняться ровно один раз для каждого элемента [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="959b5-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="959b5-142">Элемент управления [недавние элементы](windowsribbon-controls-recentitems.md) отображает список недавно использовавшихся элементов приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="959b5-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="959b5-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="959b5-143">Examples</span></span>

<span data-ttu-id="959b5-144">В следующем примере показана базовая разметка для элемента управления [недавние элементы](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="959b5-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="959b5-145">В следующем примере показано объявление команды **рецентитемс** .</span><span class="sxs-lookup"><span data-stu-id="959b5-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="959b5-146">В следующем примере показано связанное объявление элементов управления **рецентитемс** .</span><span class="sxs-lookup"><span data-stu-id="959b5-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="959b5-147">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="959b5-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="959b5-148">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="959b5-148">Minimum supported system</span></span><br/> | <span data-ttu-id="959b5-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="959b5-149">Windows 7</span></span> |
| <span data-ttu-id="959b5-150">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="959b5-150">Can be empty</span></span>                        | <span data-ttu-id="959b5-151">Да</span><span class="sxs-lookup"><span data-stu-id="959b5-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="959b5-152">См. также</span><span class="sxs-lookup"><span data-stu-id="959b5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959b5-153">Элемент управления меню приложения</span><span class="sxs-lookup"><span data-stu-id="959b5-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="959b5-154">Элемент управления "Недавние элементы"</span><span class="sxs-lookup"><span data-stu-id="959b5-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 






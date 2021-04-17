---
title: Аппликатионмену. Рецентитемс, свойство
description: Представляет контейнер для элемента управления "Недавние элементы" в меню "приложение".
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Лента Windows для свойства Аппликатионмену. Рецентитемс
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415604"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="4160f-104">Аппликатионмену. Рецентитемс, свойство</span><span class="sxs-lookup"><span data-stu-id="4160f-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="4160f-105">Представляет контейнер для элемента управления " [недавние элементы](windowsribbon-controls-recentitems.md) " в [меню "приложение](windowsribbon-controls-applicationmenu.md)".</span><span class="sxs-lookup"><span data-stu-id="4160f-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="4160f-106">Использование</span><span class="sxs-lookup"><span data-stu-id="4160f-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="4160f-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4160f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4160f-108">attribute</span><span class="sxs-lookup"><span data-stu-id="4160f-108">Attribute</span></span></th>
<th><span data-ttu-id="4160f-109">Тип</span><span class="sxs-lookup"><span data-stu-id="4160f-109">Type</span></span></th>
<th><span data-ttu-id="4160f-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4160f-110">Required</span></span></th>
<th><span data-ttu-id="4160f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4160f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4160f-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4160f-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4160f-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="4160f-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4160f-114">Нет</span><span class="sxs-lookup"><span data-stu-id="4160f-114">No</span></span><br/></td>
<td><span data-ttu-id="4160f-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4160f-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4160f-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="4160f-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4160f-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="4160f-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4160f-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="4160f-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4160f-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="4160f-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4160f-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4160f-120">Child elements</span></span>



| <span data-ttu-id="4160f-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="4160f-121">Element</span></span>                                                             | <span data-ttu-id="4160f-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4160f-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="4160f-123">**рецентитемс**</span><span class="sxs-lookup"><span data-stu-id="4160f-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="4160f-124">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="4160f-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4160f-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4160f-125">Parent elements</span></span>



| <span data-ttu-id="4160f-126">Элемент</span><span class="sxs-lookup"><span data-stu-id="4160f-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="4160f-127">**аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="4160f-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4160f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4160f-128">Remarks</span></span>

<span data-ttu-id="4160f-129">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4160f-129">Optional.</span></span>

<span data-ttu-id="4160f-130">Может встречаться не более одного раза для каждого элемента [**аппликатионмену**](windowsribbon-element-applicationmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="4160f-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="4160f-131">Элемент управления [недавние элементы](windowsribbon-controls-recentitems.md) отображает список недавно использовавшихся элементов приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="4160f-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="4160f-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="4160f-132">Examples</span></span>

<span data-ttu-id="4160f-133">В следующем примере показана базовая разметка для элемента управления [недавние элементы](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="4160f-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="4160f-134">В следующем примере показано объявление команды [**рецентитемс**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="4160f-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="4160f-135">В следующем примере показаны связанные объявления элементов управления **аппликатионмену. рецентитемс** и [**рецентитемс**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="4160f-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="4160f-136">Требования</span><span class="sxs-lookup"><span data-stu-id="4160f-136">Requirements</span></span>



| <span data-ttu-id="4160f-137">Требование</span><span class="sxs-lookup"><span data-stu-id="4160f-137">Requirement</span></span> | <span data-ttu-id="4160f-138">Значение</span><span class="sxs-lookup"><span data-stu-id="4160f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4160f-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4160f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4160f-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4160f-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4160f-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4160f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4160f-142">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4160f-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4160f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4160f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4160f-144">Элемент управления меню приложения</span><span class="sxs-lookup"><span data-stu-id="4160f-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="4160f-145">Элемент управления "Недавние элементы"</span><span class="sxs-lookup"><span data-stu-id="4160f-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 






---
title: Элемент Application
description: Представляет элемент верхнего уровня в спецификации разметки платформы Windows Ribbon.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Лента Windows для элементов приложения
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797185"
---
# <a name="application-element"></a><span data-ttu-id="b83a0-104">Элемент Application</span><span class="sxs-lookup"><span data-stu-id="b83a0-104">Application element</span></span>

<span data-ttu-id="b83a0-105">Представляет элемент верхнего уровня в спецификации разметки платформы Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="b83a0-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="b83a0-106">Использование</span><span class="sxs-lookup"><span data-stu-id="b83a0-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="b83a0-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b83a0-107">Attributes</span></span>



| <span data-ttu-id="b83a0-108">attribute</span><span class="sxs-lookup"><span data-stu-id="b83a0-108">Attribute</span></span>            | <span data-ttu-id="b83a0-109">Тип</span><span class="sxs-lookup"><span data-stu-id="b83a0-109">Type</span></span>                 | <span data-ttu-id="b83a0-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="b83a0-110">Required</span></span>       | <span data-ttu-id="b83a0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b83a0-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b83a0-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="b83a0-112">**xmlns**</span></span><br/> | <span data-ttu-id="b83a0-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b83a0-113">xs:string</span></span><br/> | <span data-ttu-id="b83a0-114">Да</span><span class="sxs-lookup"><span data-stu-id="b83a0-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="b83a0-115">Универсальный код ресурса (URI) для привязки пространства имен разметки ленты.</span><span class="sxs-lookup"><span data-stu-id="b83a0-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="b83a0-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b83a0-116">Child elements</span></span>



| <span data-ttu-id="b83a0-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="b83a0-117">Element</span></span>                                                                               | <span data-ttu-id="b83a0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b83a0-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="b83a0-119">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="b83a0-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="b83a0-120">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="b83a0-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="b83a0-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="b83a0-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="b83a0-122">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="b83a0-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b83a0-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b83a0-123">Parent elements</span></span>

<span data-ttu-id="b83a0-124">Нет родительских элементов.</span><span class="sxs-lookup"><span data-stu-id="b83a0-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="b83a0-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83a0-125">Remarks</span></span>

<span data-ttu-id="b83a0-126">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b83a0-126">Required.</span></span>

<span data-ttu-id="b83a0-127">Должен выполняться ровно один раз в качестве контейнера для всей разметки ленты.</span><span class="sxs-lookup"><span data-stu-id="b83a0-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="b83a0-128">Дочерние элементы элемента **Application** должны находиться в указанном порядке:</span><span class="sxs-lookup"><span data-stu-id="b83a0-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="b83a0-129">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="b83a0-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="b83a0-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="b83a0-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="b83a0-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="b83a0-131">Examples</span></span>

<span data-ttu-id="b83a0-132">В следующем примере показано объявление элемента **приложения** .</span><span class="sxs-lookup"><span data-stu-id="b83a0-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="b83a0-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b83a0-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b83a0-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="b83a0-134">Minimum supported system</span></span><br/> | <span data-ttu-id="b83a0-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b83a0-135">Windows 7</span></span> |
| <span data-ttu-id="b83a0-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="b83a0-136">Can be empty</span></span>                        | <span data-ttu-id="b83a0-137">Нет</span><span class="sxs-lookup"><span data-stu-id="b83a0-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="b83a0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b83a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83a0-139">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="b83a0-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 






---
description: Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: Субскриптионидлфунктиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912220"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="9bbff-103">Субскриптионидлфунктиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="9bbff-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="9bbff-104">Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="9bbff-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9bbff-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9bbff-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="9bbff-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9bbff-106">Attributes</span></span>



| <span data-ttu-id="9bbff-107">attribute</span><span class="sxs-lookup"><span data-stu-id="9bbff-107">Attribute</span></span>                 | <span data-ttu-id="9bbff-108">Тип</span><span class="sxs-lookup"><span data-stu-id="9bbff-108">Type</span></span>               | <span data-ttu-id="9bbff-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9bbff-109">Required</span></span>      | <span data-ttu-id="9bbff-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9bbff-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbff-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="9bbff-111">**extensible**</span></span><br/> | <span data-ttu-id="9bbff-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="9bbff-112">boolean</span></span><br/> | <span data-ttu-id="9bbff-113">Нет</span><span class="sxs-lookup"><span data-stu-id="9bbff-113">No</span></span><br/> | <span data-ttu-id="9bbff-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="9bbff-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="9bbff-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="9bbff-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="9bbff-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9bbff-116">Child elements</span></span>



| <span data-ttu-id="9bbff-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="9bbff-117">Element</span></span>                                                           | <span data-ttu-id="9bbff-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9bbff-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bbff-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="9bbff-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="9bbff-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="9bbff-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="9bbff-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="9bbff-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="9bbff-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="9bbff-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="9bbff-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="9bbff-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="9bbff-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="9bbff-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="9bbff-125">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="9bbff-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9bbff-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9bbff-126">Parent elements</span></span>



| <span data-ttu-id="9bbff-127">Элемент</span><span class="sxs-lookup"><span data-stu-id="9bbff-127">Element</span></span>                         | <span data-ttu-id="9bbff-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9bbff-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9bbff-129">**File**</span><span class="sxs-lookup"><span data-stu-id="9bbff-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9bbff-130">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="9bbff-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9bbff-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9bbff-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9bbff-132">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9bbff-132">Minimum supported system</span></span><br/> | <span data-ttu-id="9bbff-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bbff-133">Windows Vista</span></span> |
| <span data-ttu-id="9bbff-134">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9bbff-134">Can be empty</span></span>                        | <span data-ttu-id="9bbff-135">Да</span><span class="sxs-lookup"><span data-stu-id="9bbff-135">Yes</span></span>           |



 

 





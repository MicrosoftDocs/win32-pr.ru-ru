---
description: Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: Субскриптионфунктиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273075"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="74919-103">Субскриптионфунктиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="74919-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="74919-104">Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="74919-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="74919-105">Использование</span><span class="sxs-lookup"><span data-stu-id="74919-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="74919-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="74919-106">Attributes</span></span>



| <span data-ttu-id="74919-107">attribute</span><span class="sxs-lookup"><span data-stu-id="74919-107">Attribute</span></span>                 | <span data-ttu-id="74919-108">Тип</span><span class="sxs-lookup"><span data-stu-id="74919-108">Type</span></span>               | <span data-ttu-id="74919-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="74919-109">Required</span></span>      | <span data-ttu-id="74919-110">Описание</span><span class="sxs-lookup"><span data-stu-id="74919-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74919-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="74919-111">**extensible**</span></span><br/> | <span data-ttu-id="74919-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="74919-112">boolean</span></span><br/> | <span data-ttu-id="74919-113">Нет</span><span class="sxs-lookup"><span data-stu-id="74919-113">No</span></span><br/> | <span data-ttu-id="74919-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="74919-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="74919-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="74919-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="74919-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="74919-116">Child elements</span></span>



| <span data-ttu-id="74919-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="74919-117">Element</span></span>                                                           | <span data-ttu-id="74919-118">Описание</span><span class="sxs-lookup"><span data-stu-id="74919-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74919-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="74919-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="74919-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="74919-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="74919-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="74919-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="74919-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="74919-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="74919-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="74919-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="74919-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="74919-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="74919-125">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="74919-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="74919-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="74919-126">Parent elements</span></span>



| <span data-ttu-id="74919-127">Элемент</span><span class="sxs-lookup"><span data-stu-id="74919-127">Element</span></span>                         | <span data-ttu-id="74919-128">Описание</span><span class="sxs-lookup"><span data-stu-id="74919-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="74919-129">**File**</span><span class="sxs-lookup"><span data-stu-id="74919-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="74919-130">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="74919-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="74919-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="74919-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="74919-132">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="74919-132">Minimum supported system</span></span><br/> | <span data-ttu-id="74919-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74919-133">Windows Vista</span></span> |
| <span data-ttu-id="74919-134">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="74919-134">Can be empty</span></span>                        | <span data-ttu-id="74919-135">Да</span><span class="sxs-lookup"><span data-stu-id="74919-135">Yes</span></span>           |



 

 





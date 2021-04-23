---
description: Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: Субскриптионпроксифунктионимплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144926"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="724db-103">Субскриптионпроксифунктионимплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="724db-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="724db-104">Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="724db-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="724db-105">Использование</span><span class="sxs-lookup"><span data-stu-id="724db-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="724db-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="724db-106">Attributes</span></span>



| <span data-ttu-id="724db-107">attribute</span><span class="sxs-lookup"><span data-stu-id="724db-107">Attribute</span></span>                 | <span data-ttu-id="724db-108">Тип</span><span class="sxs-lookup"><span data-stu-id="724db-108">Type</span></span>               | <span data-ttu-id="724db-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="724db-109">Required</span></span>      | <span data-ttu-id="724db-110">Описание</span><span class="sxs-lookup"><span data-stu-id="724db-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724db-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="724db-111">**extensible**</span></span><br/> | <span data-ttu-id="724db-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="724db-112">boolean</span></span><br/> | <span data-ttu-id="724db-113">Нет</span><span class="sxs-lookup"><span data-stu-id="724db-113">No</span></span><br/> | <span data-ttu-id="724db-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="724db-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="724db-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="724db-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="724db-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="724db-116">Child elements</span></span>



| <span data-ttu-id="724db-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="724db-117">Element</span></span>                                                           | <span data-ttu-id="724db-118">Описание</span><span class="sxs-lookup"><span data-stu-id="724db-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="724db-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="724db-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="724db-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="724db-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="724db-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="724db-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="724db-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="724db-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="724db-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="724db-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="724db-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="724db-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="724db-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="724db-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="724db-126">Указывает имя класса прокси на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="724db-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="724db-127">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="724db-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="724db-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="724db-128">Parent elements</span></span>



| <span data-ttu-id="724db-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="724db-129">Element</span></span>                         | <span data-ttu-id="724db-130">Описание</span><span class="sxs-lookup"><span data-stu-id="724db-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="724db-131">**File**</span><span class="sxs-lookup"><span data-stu-id="724db-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="724db-132">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="724db-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="724db-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="724db-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="724db-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="724db-134">Minimum supported system</span></span><br/> | <span data-ttu-id="724db-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="724db-135">Windows Vista</span></span> |
| <span data-ttu-id="724db-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="724db-136">Can be empty</span></span>                        | <span data-ttu-id="724db-137">Да</span><span class="sxs-lookup"><span data-stu-id="724db-137">Yes</span></span>           |



 

 





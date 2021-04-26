---
description: Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: Субскриптионпроксифунктионимплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995321"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="8f8ad-103">Субскриптионпроксифунктионимплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="8f8ad-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="8f8ad-104">Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="8f8ad-105">Использование</span><span class="sxs-lookup"><span data-stu-id="8f8ad-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="8f8ad-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f8ad-106">Attributes</span></span>



| <span data-ttu-id="8f8ad-107">attribute</span><span class="sxs-lookup"><span data-stu-id="8f8ad-107">Attribute</span></span>                 | <span data-ttu-id="8f8ad-108">Тип</span><span class="sxs-lookup"><span data-stu-id="8f8ad-108">Type</span></span>               | <span data-ttu-id="8f8ad-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="8f8ad-109">Required</span></span>      | <span data-ttu-id="8f8ad-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8f8ad-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8ad-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-111">**extensible**</span></span><br/> | <span data-ttu-id="8f8ad-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="8f8ad-112">boolean</span></span><br/> | <span data-ttu-id="8f8ad-113">нет</span><span class="sxs-lookup"><span data-stu-id="8f8ad-113">No</span></span><br/> | <span data-ttu-id="8f8ad-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="8f8ad-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8f8ad-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8f8ad-116">Child elements</span></span>



| <span data-ttu-id="8f8ad-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="8f8ad-117">Element</span></span>                                                           | <span data-ttu-id="8f8ad-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8f8ad-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f8ad-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="8f8ad-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="8f8ad-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="8f8ad-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="8f8ad-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="8f8ad-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="8f8ad-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="8f8ad-126">Указывает имя класса прокси на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="8f8ad-127">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="8f8ad-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8f8ad-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8f8ad-128">Parent elements</span></span>



| <span data-ttu-id="8f8ad-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="8f8ad-129">Element</span></span>                         | <span data-ttu-id="8f8ad-130">Описание</span><span class="sxs-lookup"><span data-stu-id="8f8ad-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8f8ad-131">**File**</span><span class="sxs-lookup"><span data-stu-id="8f8ad-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8f8ad-132">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="8f8ad-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8f8ad-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f8ad-133">Element information</span></span>



| <span data-ttu-id="8f8ad-134">Метка</span><span class="sxs-lookup"><span data-stu-id="8f8ad-134">Label</span></span> | <span data-ttu-id="8f8ad-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8f8ad-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8f8ad-136">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="8f8ad-136">Minimum supported system</span></span><br/> | <span data-ttu-id="8f8ad-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f8ad-137">Windows Vista</span></span> |
| <span data-ttu-id="8f8ad-138">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="8f8ad-138">Can be empty</span></span>                        | <span data-ttu-id="8f8ad-139">Да</span><span class="sxs-lookup"><span data-stu-id="8f8ad-139">Yes</span></span>           |



 

 





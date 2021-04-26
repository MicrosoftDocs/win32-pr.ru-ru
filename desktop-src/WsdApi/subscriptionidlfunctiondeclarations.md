---
description: Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: Субскриптионидлфунктиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d738dd06ccbf034702cbb7d6494a28a229d07
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995371"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="485af-103">Субскриптионидлфунктиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="485af-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="485af-104">Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="485af-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="485af-105">Использование</span><span class="sxs-lookup"><span data-stu-id="485af-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="485af-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="485af-106">Attributes</span></span>



| <span data-ttu-id="485af-107">attribute</span><span class="sxs-lookup"><span data-stu-id="485af-107">Attribute</span></span>                 | <span data-ttu-id="485af-108">Тип</span><span class="sxs-lookup"><span data-stu-id="485af-108">Type</span></span>               | <span data-ttu-id="485af-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="485af-109">Required</span></span>      | <span data-ttu-id="485af-110">Описание</span><span class="sxs-lookup"><span data-stu-id="485af-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="485af-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="485af-111">**extensible**</span></span><br/> | <span data-ttu-id="485af-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="485af-112">boolean</span></span><br/> | <span data-ttu-id="485af-113">нет</span><span class="sxs-lookup"><span data-stu-id="485af-113">No</span></span><br/> | <span data-ttu-id="485af-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="485af-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="485af-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="485af-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="485af-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="485af-116">Child elements</span></span>



| <span data-ttu-id="485af-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="485af-117">Element</span></span>                                                           | <span data-ttu-id="485af-118">Описание</span><span class="sxs-lookup"><span data-stu-id="485af-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="485af-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="485af-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="485af-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="485af-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="485af-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="485af-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="485af-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="485af-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="485af-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="485af-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="485af-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="485af-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="485af-125">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="485af-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="485af-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="485af-126">Parent elements</span></span>



| <span data-ttu-id="485af-127">Элемент</span><span class="sxs-lookup"><span data-stu-id="485af-127">Element</span></span>                         | <span data-ttu-id="485af-128">Описание</span><span class="sxs-lookup"><span data-stu-id="485af-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="485af-129">**File**</span><span class="sxs-lookup"><span data-stu-id="485af-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="485af-130">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="485af-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="485af-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="485af-131">Element information</span></span>



| <span data-ttu-id="485af-132">Метка</span><span class="sxs-lookup"><span data-stu-id="485af-132">Label</span></span> | <span data-ttu-id="485af-133">Значение</span><span class="sxs-lookup"><span data-stu-id="485af-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="485af-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="485af-134">Minimum supported system</span></span><br/> | <span data-ttu-id="485af-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="485af-135">Windows Vista</span></span> |
| <span data-ttu-id="485af-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="485af-136">Can be empty</span></span>                        | <span data-ttu-id="485af-137">Да</span><span class="sxs-lookup"><span data-stu-id="485af-137">Yes</span></span>           |



 

 





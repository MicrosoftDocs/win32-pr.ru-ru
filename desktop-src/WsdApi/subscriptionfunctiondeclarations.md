---
description: Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: Субскриптионфунктиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995461"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="d4491-103">Субскриптионфунктиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="d4491-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="d4491-104">Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="d4491-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="d4491-105">Использование</span><span class="sxs-lookup"><span data-stu-id="d4491-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="d4491-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d4491-106">Attributes</span></span>



| <span data-ttu-id="d4491-107">attribute</span><span class="sxs-lookup"><span data-stu-id="d4491-107">Attribute</span></span>                 | <span data-ttu-id="d4491-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d4491-108">Type</span></span>               | <span data-ttu-id="d4491-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d4491-109">Required</span></span>      | <span data-ttu-id="d4491-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d4491-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4491-111">**легко**</span><span class="sxs-lookup"><span data-stu-id="d4491-111">**extensible**</span></span><br/> | <span data-ttu-id="d4491-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="d4491-112">boolean</span></span><br/> | <span data-ttu-id="d4491-113">нет</span><span class="sxs-lookup"><span data-stu-id="d4491-113">No</span></span><br/> | <span data-ttu-id="d4491-114">Возможность добавлять точки расширения в функции и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d4491-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="d4491-115">Это значение всегда равно true.</span><span class="sxs-lookup"><span data-stu-id="d4491-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="d4491-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d4491-116">Child elements</span></span>



| <span data-ttu-id="d4491-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4491-117">Element</span></span>                                                           | <span data-ttu-id="d4491-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d4491-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4491-119">**нотификатионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="d4491-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="d4491-120">Указывает имя интерфейса уведомления, используемого с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="d4491-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="d4491-121">**операцию**</span><span class="sxs-lookup"><span data-stu-id="d4491-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="d4491-122">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="d4491-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="d4491-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="d4491-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="d4491-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="d4491-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="d4491-125">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="d4491-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="d4491-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d4491-126">Parent elements</span></span>



| <span data-ttu-id="d4491-127">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4491-127">Element</span></span>                         | <span data-ttu-id="d4491-128">Описание</span><span class="sxs-lookup"><span data-stu-id="d4491-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d4491-129">**File**</span><span class="sxs-lookup"><span data-stu-id="d4491-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d4491-130">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="d4491-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d4491-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d4491-131">Element information</span></span>



| <span data-ttu-id="d4491-132">Метка</span><span class="sxs-lookup"><span data-stu-id="d4491-132">Label</span></span> | <span data-ttu-id="d4491-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d4491-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d4491-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="d4491-134">Minimum supported system</span></span><br/> | <span data-ttu-id="d4491-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4491-135">Windows Vista</span></span> |
| <span data-ttu-id="d4491-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="d4491-136">Can be empty</span></span>                        | <span data-ttu-id="d4491-137">Да</span><span class="sxs-lookup"><span data-stu-id="d4491-137">Yes</span></span>           |



 

 





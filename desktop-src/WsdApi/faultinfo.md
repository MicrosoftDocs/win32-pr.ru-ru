---
description: Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: Фаултинфо, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264992"
---
# <a name="faultinfo-element"></a><span data-ttu-id="1efb8-103">Фаултинфо, элемент</span><span class="sxs-lookup"><span data-stu-id="1efb8-103">faultInfo element</span></span>

<span data-ttu-id="1efb8-104">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1efb8-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="1efb8-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1efb8-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="1efb8-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1efb8-106">Attributes</span></span>

<span data-ttu-id="1efb8-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1efb8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1efb8-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1efb8-108">Child elements</span></span>

<span data-ttu-id="1efb8-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="1efb8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1efb8-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1efb8-110">Parent elements</span></span>



| <span data-ttu-id="1efb8-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="1efb8-111">Element</span></span>                                                                         | <span data-ttu-id="1efb8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1efb8-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1efb8-113">**функтиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="1efb8-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="1efb8-114">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="1efb8-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="1efb8-115">**идлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="1efb8-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="1efb8-116">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="1efb8-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="1efb8-117">**проксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="1efb8-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="1efb8-118">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="1efb8-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="1efb8-119">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="1efb8-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="1efb8-120">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="1efb8-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="1efb8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1efb8-121">Remarks</span></span>

<span data-ttu-id="1efb8-122">Возможные значения: 1 (параметры ошибок включены) и 0 (параметры ошибки исключены).</span><span class="sxs-lookup"><span data-stu-id="1efb8-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="1efb8-123">По умолчанию параметры ошибки исключаются.</span><span class="sxs-lookup"><span data-stu-id="1efb8-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="1efb8-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1efb8-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1efb8-125">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1efb8-125">Minimum supported system</span></span><br/> | <span data-ttu-id="1efb8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1efb8-126">Windows Vista</span></span> |
| <span data-ttu-id="1efb8-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1efb8-127">Can be empty</span></span>                        | <span data-ttu-id="1efb8-128">Да</span><span class="sxs-lookup"><span data-stu-id="1efb8-128">Yes</span></span>           |



 

 





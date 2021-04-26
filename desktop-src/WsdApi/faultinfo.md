---
description: Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: Фаултинфо, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995861"
---
# <a name="faultinfo-element"></a><span data-ttu-id="35194-103">Фаултинфо, элемент</span><span class="sxs-lookup"><span data-stu-id="35194-103">faultInfo element</span></span>

<span data-ttu-id="35194-104">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="35194-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="35194-105">Использование</span><span class="sxs-lookup"><span data-stu-id="35194-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="35194-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="35194-106">Attributes</span></span>

<span data-ttu-id="35194-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="35194-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="35194-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="35194-108">Child elements</span></span>

<span data-ttu-id="35194-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="35194-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="35194-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="35194-110">Parent elements</span></span>



| <span data-ttu-id="35194-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="35194-111">Element</span></span>                                                                         | <span data-ttu-id="35194-112">Описание</span><span class="sxs-lookup"><span data-stu-id="35194-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35194-113">**функтиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="35194-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="35194-114">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="35194-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="35194-115">**идлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="35194-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="35194-116">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="35194-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="35194-117">**проксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="35194-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="35194-118">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="35194-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="35194-119">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="35194-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="35194-120">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="35194-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="35194-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="35194-121">Remarks</span></span>

<span data-ttu-id="35194-122">Возможные значения: 1 (параметры ошибок включены) и 0 (параметры ошибки исключены).</span><span class="sxs-lookup"><span data-stu-id="35194-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="35194-123">По умолчанию параметры ошибки исключаются.</span><span class="sxs-lookup"><span data-stu-id="35194-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="35194-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="35194-124">Element information</span></span>



| <span data-ttu-id="35194-125">Метка</span><span class="sxs-lookup"><span data-stu-id="35194-125">Label</span></span> | <span data-ttu-id="35194-126">Значение</span><span class="sxs-lookup"><span data-stu-id="35194-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="35194-127">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="35194-127">Minimum supported system</span></span><br/> | <span data-ttu-id="35194-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35194-128">Windows Vista</span></span> |
| <span data-ttu-id="35194-129">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="35194-129">Can be empty</span></span>                        | <span data-ttu-id="35194-130">Да</span><span class="sxs-lookup"><span data-stu-id="35194-130">Yes</span></span>           |



 

 





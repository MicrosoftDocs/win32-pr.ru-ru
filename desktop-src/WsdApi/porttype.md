---
description: Указывает тип порта, для которого создается код.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: элемент portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996541"
---
# <a name="porttype-element"></a><span data-ttu-id="b7194-103">элемент portType</span><span class="sxs-lookup"><span data-stu-id="b7194-103">portType element</span></span>

<span data-ttu-id="b7194-104">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="b7194-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="b7194-105">Использование</span><span class="sxs-lookup"><span data-stu-id="b7194-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="b7194-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7194-106">Attributes</span></span>

<span data-ttu-id="b7194-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b7194-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b7194-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7194-108">Child elements</span></span>

<span data-ttu-id="b7194-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b7194-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b7194-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7194-110">Parent elements</span></span>



| <span data-ttu-id="b7194-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7194-111">Element</span></span>                                                                                                 | <span data-ttu-id="b7194-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b7194-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7194-113">**функтиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="b7194-114">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="b7194-115">**идлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="b7194-116">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="b7194-117">**мессажеструктуредефинитионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="b7194-118">Создает определения структуры C для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7194-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="b7194-119">**мессажетипедекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="b7194-120">Создает объявления констант C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7194-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="b7194-121">**мессажетипедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="b7194-122">Создает константы C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="b7194-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="b7194-123">**порттипедекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="b7194-124">Создает объявления констант C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="b7194-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="b7194-125">**порттипедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="b7194-126">Создает константы C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="b7194-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="b7194-127">**проксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="b7194-128">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="b7194-129">**стубдекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="b7194-130">Создает объявления для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="b7194-131">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="b7194-132">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="b7194-133">**субскриптионфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="b7194-134">Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b7194-135">**субскриптионидлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b7194-136">Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b7194-137">**субскриптионпроксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="b7194-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="b7194-138">Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="b7194-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b7194-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7194-139">Remarks</span></span>

<span data-ttu-id="b7194-140">По умолчанию код создается для всех типов портов во входных файлах WSDL.</span><span class="sxs-lookup"><span data-stu-id="b7194-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="b7194-141">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7194-141">Element information</span></span>



| <span data-ttu-id="b7194-142">Метка</span><span class="sxs-lookup"><span data-stu-id="b7194-142">Label</span></span> | <span data-ttu-id="b7194-143">Значение</span><span class="sxs-lookup"><span data-stu-id="b7194-143">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b7194-144">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="b7194-144">Minimum supported system</span></span><br/> | <span data-ttu-id="b7194-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7194-145">Windows Vista</span></span> |
| <span data-ttu-id="b7194-146">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="b7194-146">Can be empty</span></span>                        | <span data-ttu-id="b7194-147">Да</span><span class="sxs-lookup"><span data-stu-id="b7194-147">Yes</span></span>           |



 

 





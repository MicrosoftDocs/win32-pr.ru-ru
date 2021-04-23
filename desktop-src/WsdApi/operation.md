---
description: Указывает операцию, для которой создается код.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation, элемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080578"
---
# <a name="operation-element"></a><span data-ttu-id="157db-103">Operation, элемент</span><span class="sxs-lookup"><span data-stu-id="157db-103">operation element</span></span>

<span data-ttu-id="157db-104">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="157db-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="157db-105">Использование</span><span class="sxs-lookup"><span data-stu-id="157db-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="157db-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="157db-106">Attributes</span></span>

<span data-ttu-id="157db-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="157db-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="157db-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="157db-108">Child elements</span></span>

<span data-ttu-id="157db-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="157db-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="157db-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="157db-110">Parent elements</span></span>



| <span data-ttu-id="157db-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="157db-111">Element</span></span>                                                                                                 | <span data-ttu-id="157db-112">Описание</span><span class="sxs-lookup"><span data-stu-id="157db-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="157db-113">**функтиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="157db-114">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="157db-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="157db-115">**идлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="157db-116">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="157db-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="157db-117">**мессажеструктуредефинитионс**</span><span class="sxs-lookup"><span data-stu-id="157db-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="157db-118">Создает определения структуры C для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="157db-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="157db-119">**мессажетипедекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="157db-120">Создает объявления констант C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="157db-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="157db-121">**мессажетипедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="157db-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="157db-122">Создает константы C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="157db-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="157db-123">**порттипедекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="157db-124">Создает объявления констант C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="157db-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="157db-125">**порттипедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="157db-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="157db-126">Создает константы C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="157db-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="157db-127">**проксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="157db-128">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="157db-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="157db-129">**стубдекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="157db-130">Создает объявления для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="157db-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="157db-131">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="157db-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="157db-132">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="157db-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="157db-133">**субскриптионфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="157db-134">Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="157db-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="157db-135">**субскриптионидлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="157db-136">Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="157db-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="157db-137">**субскриптионпроксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="157db-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="157db-138">Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.</span><span class="sxs-lookup"><span data-stu-id="157db-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="157db-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="157db-139">Remarks</span></span>

<span data-ttu-id="157db-140">Можно указать любое количество операций.</span><span class="sxs-lookup"><span data-stu-id="157db-140">Any number of operations may be specified.</span></span> <span data-ttu-id="157db-141">Если операции не указаны, код создается для всех операций во всех соответствующих типах портов.</span><span class="sxs-lookup"><span data-stu-id="157db-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="157db-142">Использование элемента **Operation** ограничит методы, созданные для тех, которые содержатся в операции.</span><span class="sxs-lookup"><span data-stu-id="157db-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="157db-143">Например, принтер поддерживает следующие операции:</span><span class="sxs-lookup"><span data-stu-id="157db-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="157db-144">**принтжоббипост**</span><span class="sxs-lookup"><span data-stu-id="157db-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="157db-145">**принтжоббиреференце**</span><span class="sxs-lookup"><span data-stu-id="157db-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="157db-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="157db-146">**CancelJob**</span></span>
-   <span data-ttu-id="157db-147">**жетжобелементс**</span><span class="sxs-lookup"><span data-stu-id="157db-147">**GetJobElements**</span></span>
-   <span data-ttu-id="157db-148">**жетактивежобс**</span><span class="sxs-lookup"><span data-stu-id="157db-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="157db-149">**жетжобхистори**</span><span class="sxs-lookup"><span data-stu-id="157db-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="157db-150">**субскрибетопринтерконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="157db-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="157db-151">**унсубскрибетопринтерконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="157db-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="157db-152">Однако, чтобы включить только методы, связанные с операциями **принтжоббипост** и **жетжобелементс** , скрипт создания кода будет использовать элементы [**идлфунктиондекларатионс**](idlfunctiondeclarations.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="157db-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="157db-153">При этом создаются объявления функций IDL для всех методов, связанных с двумя операциями (например, **бегинпринтжоббипост**, **ендпринтжоббипост**, **бегинжетжобелементс** и **енджетжобелементс**).</span><span class="sxs-lookup"><span data-stu-id="157db-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="157db-154">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="157db-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="157db-155">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="157db-155">Minimum supported system</span></span><br/> | <span data-ttu-id="157db-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="157db-156">Windows Vista</span></span> |
| <span data-ttu-id="157db-157">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="157db-157">Can be empty</span></span>                        | <span data-ttu-id="157db-158">Да</span><span class="sxs-lookup"><span data-stu-id="157db-158">Yes</span></span>           |



 

 





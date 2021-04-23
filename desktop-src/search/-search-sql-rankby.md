---
description: Результаты запроса включают строки, возвращаемые запросом, и значение ранга для каждой строки, если столбец Rank включен в предложение SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: РАНЖИРОВАНие по предложению
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262936"
---
# <a name="rank-by-clause"></a><span data-ttu-id="f5bc5-103">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="f5bc5-103">RANK BY Clause</span></span>

<span data-ttu-id="f5bc5-104">Результаты запроса включают строки, возвращаемые запросом, и значение ранга для каждой строки, если столбец Rank включен в предложение SELECT.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="f5bc5-105">Значения ранжирования рассчитываются поисковой системой и возвращаются в виде целых чисел в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="f5bc5-106">Чтобы повысить осмысленность результатов ранжирования, запрос может управлять вычислением необработанных значений ранжирования в предложении RANK BY.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="f5bc5-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f5bc5-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f5bc5-108">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="f5bc5-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="f5bc5-109">WEIGHT, функция</span><span class="sxs-lookup"><span data-stu-id="f5bc5-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="f5bc5-110">Функция ПРИВЕДЕНия</span><span class="sxs-lookup"><span data-stu-id="f5bc5-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="f5bc5-111">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="f5bc5-111">RANK BY Clause</span></span>

<span data-ttu-id="f5bc5-112">Синтаксис для предложения RANK BY выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f5bc5-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="f5bc5-113">Предложение RANK BY применяется к \_ условию поиска, непосредственно предшествующему ему, фактически задающему более низкий или более высокий ранг строк, возвращаемых условием поиска, чем строки, возвращенные другим условием поиска.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="f5bc5-114">Обязательные круглые скобки, окружающие \_ условие поиска.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="f5bc5-115">Круглые скобки, окружающие спецификацию ранга, являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="f5bc5-116">К одному условию можно применить более одного предложения RANK BY.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="f5bc5-117">Дополнительные предложения RANK можно включить один за другим с помощью круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="f5bc5-118">Полнотекстовые предикаты возвращают значения ранга в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="f5bc5-119">Значения ранга для всех документов, совпадающих с неполнотекстовым предикатом, — 1000.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="f5bc5-120">Изменения ранговых значений должны учитывать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="f5bc5-121">Спецификация Rank в \_ предложении ранкби определяет одну или несколько функций, применяемых к значениям ранга.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="f5bc5-122">Функция WEIGHT применяет множитель к необработанному значению ранга для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="f5bc5-123">Чем меньше множитель, тем меньше результирующее значение ранга.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="f5bc5-124">Функцию ПРИВЕДЕНия можно использовать для умножения, добавления в или задания определенного значения ранга для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="f5bc5-125">Каждая спецификация ранжирования может включать либо нуль, либо одну функцию веса, а также ноль или более функций ПРИВЕДЕНия.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="f5bc5-126">Если в предложении РАНЖИРОВАНия включены функции веса и ПРИВЕДЕНия, функция WEIGHT должна быть первой.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="f5bc5-127">WEIGHT, функция</span><span class="sxs-lookup"><span data-stu-id="f5bc5-127">WEIGHT Function</span></span>

<span data-ttu-id="f5bc5-128">Синтаксис функции WEIGHT:</span><span class="sxs-lookup"><span data-stu-id="f5bc5-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="f5bc5-129">Множитель должен быть десятичным числом от 0,001 до 1,000.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="f5bc5-130">Необработанное значение ранга, возвращаемое предикатом условия поиска, умножается на коэффициент веса, чтобы задать новое значение ранга.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="f5bc5-131">В следующем примере функция WEIGHT предоставляет документам слово «Сереса» в System.Docумент. Ластаусор поле половины значение ранга документов с "Сереса" в поле System. author:</span><span class="sxs-lookup"><span data-stu-id="f5bc5-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="f5bc5-132">Функции взвешивания столбцов предикатов CONTAINS и FREETEXT поддерживают сокращенный формат с помощью двоеточия между поисковым условием и множителем ("программное обеспечение": 0,25).</span><span class="sxs-lookup"><span data-stu-id="f5bc5-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="f5bc5-133">Предложение RANK BY не поддерживает сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="f5bc5-134">При использовании РАНЖИРОВАНия по ВЕСУ существует ограничение: оно не работает с предложениями CONTAINS, которые используют логические условия. Например, следующий пример не разрешен:</span><span class="sxs-lookup"><span data-stu-id="f5bc5-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="f5bc5-135">Функция ПРИВЕДЕНия</span><span class="sxs-lookup"><span data-stu-id="f5bc5-135">COERCION Function</span></span>

<span data-ttu-id="f5bc5-136">Функцию приведения рангов можно использовать для изменения возвращаемого значения ранга путем сложения или умножения или присвоения ему определенного значения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="f5bc5-137">Синтаксис функции ПРИВЕДЕН ниже.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="f5bc5-138">Значение приведения является целочисленным значением.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="f5bc5-139">В следующей таблице описаны доступные параметры операции приведения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="f5bc5-140">Операция приведения</span><span class="sxs-lookup"><span data-stu-id="f5bc5-140">Coercion operation</span></span> | <span data-ttu-id="f5bc5-141">Описание</span><span class="sxs-lookup"><span data-stu-id="f5bc5-141">Description</span></span>                                                                                    | <span data-ttu-id="f5bc5-142">Диапазон значений</span><span class="sxs-lookup"><span data-stu-id="f5bc5-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="f5bc5-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="f5bc5-143">ABSOLUTE</span></span>           | <span data-ttu-id="f5bc5-144">Возвращаемое значение ранга — это значение, указанное в значении приведения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="f5bc5-145">от 0 до 1000</span><span class="sxs-lookup"><span data-stu-id="f5bc5-145">0 to 1000</span></span>    |
| <span data-ttu-id="f5bc5-146">ADD</span><span class="sxs-lookup"><span data-stu-id="f5bc5-146">ADD</span></span>                | <span data-ttu-id="f5bc5-147">Возвращаемое значение ранга является суммой необработанного значения ранга и указанного значения приведения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="f5bc5-148">от 0,001 до 1,0</span><span class="sxs-lookup"><span data-stu-id="f5bc5-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="f5bc5-149">MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="f5bc5-149">MULTIPLY</span></span>           | <span data-ttu-id="f5bc5-150">Возвращаемое значение ранга — это произведение необработанного значения ранга и указанного значения приведения.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="f5bc5-151">от 0,001 до 1,0</span><span class="sxs-lookup"><span data-stu-id="f5bc5-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="f5bc5-152">Поиск может возвращать значения ранга только в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="f5bc5-153">В следующем примере функция ПРИВЕДЕНия используется для установки для всех документов с именем "Computer", равным 1000, при сокращении на один квартал ранг документов, содержащих как "Computer", так и "программное обеспечение" в заголовке.</span><span class="sxs-lookup"><span data-stu-id="f5bc5-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 




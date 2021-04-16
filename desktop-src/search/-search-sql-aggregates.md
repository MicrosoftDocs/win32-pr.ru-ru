---
description: Агрегатная функция выполняет вычисление для набора значений и возвращает значение. Это позволяет создавать сводные статистические данные для многоуровневых групп с небольшими издержками.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Агрегатные функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570695"
---
# <a name="aggregate-functions"></a><span data-ttu-id="c68fb-104">Агрегатные функции</span><span class="sxs-lookup"><span data-stu-id="c68fb-104">Aggregate Functions</span></span>

<span data-ttu-id="c68fb-105">Агрегатная функция выполняет вычисление для набора значений и возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c68fb-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="c68fb-106">Это позволяет создавать сводные статистические данные для многоуровневых групп с небольшими издержками.</span><span class="sxs-lookup"><span data-stu-id="c68fb-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="c68fb-107">Общие сведения о агрегатных функциях</span><span class="sxs-lookup"><span data-stu-id="c68fb-107">About Aggregate Functions</span></span>

<span data-ttu-id="c68fb-108">Агрегатные функции в Windows Search язык SQL (SQL) имеют следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="c68fb-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="c68fb-109">Часть функции может содержать любую из следующих функций и синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c68fb-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="c68fb-110">Функция</span><span class="sxs-lookup"><span data-stu-id="c68fb-110">Function</span></span>                                                              | <span data-ttu-id="c68fb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c68fb-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68fb-112">AVG ( <column> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="c68fb-113">Возвращает среднее арифметическое значений в группе.</span><span class="sxs-lookup"><span data-stu-id="c68fb-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="c68fb-114">Применяется только к числам.</span><span class="sxs-lookup"><span data-stu-id="c68fb-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="c68fb-115">БИФРЕКУЕНЦИ ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="c68fb-116">Возвращает наиболее частое значение столбца N из результатов в группе.</span><span class="sxs-lookup"><span data-stu-id="c68fb-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="c68fb-117">Также содержит количество раз, когда произошло каждое значение, и идентификаторы документов для результатов, содержащих каждое возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="c68fb-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="c68fb-118">CHILDCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="c68fb-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="c68fb-119">Возвращает число элементов в группе (за исключением подгрупп).</span><span class="sxs-lookup"><span data-stu-id="c68fb-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="c68fb-120">Если имеется несколько уровней группировки, возвращается число непосредственных дочерних групп.</span><span class="sxs-lookup"><span data-stu-id="c68fb-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="c68fb-121">COUNT ()</span><span class="sxs-lookup"><span data-stu-id="c68fb-121">COUNT()</span></span>                                                               | <span data-ttu-id="c68fb-122">Возвращает количество элементов в группе и всех подгрупп.</span><span class="sxs-lookup"><span data-stu-id="c68fb-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c68fb-123">DATERANGE ( <column> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="c68fb-124">Возвращает нижнюю и верхнюю границы значений столбцов, найденных в группе результатов группы.</span><span class="sxs-lookup"><span data-stu-id="c68fb-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="c68fb-125">Допустимо только для свойств FILETIME.</span><span class="sxs-lookup"><span data-stu-id="c68fb-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="c68fb-126">FIRST ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="c68fb-127">Возвращает первые N значений столбцов из конечных результатов, найденных в группе.</span><span class="sxs-lookup"><span data-stu-id="c68fb-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="c68fb-128">MAX ( <column> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="c68fb-129">Возвращает максимальное значение выражения.</span><span class="sxs-lookup"><span data-stu-id="c68fb-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="c68fb-130">Применимо только к числам или датам.</span><span class="sxs-lookup"><span data-stu-id="c68fb-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="c68fb-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="c68fb-132">Возвращает минимальное значение выражения.</span><span class="sxs-lookup"><span data-stu-id="c68fb-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="c68fb-133">Применимо только к числам или датам.</span><span class="sxs-lookup"><span data-stu-id="c68fb-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="c68fb-134">РЕПРЕСЕНТАТИВЕОФ ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="c68fb-135">Возвращает N значений Идрепресентативе, каждое из которых выбрано из одного из подмножеств результатов, имеющих уникальное значение столбца.</span><span class="sxs-lookup"><span data-stu-id="c68fb-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="c68fb-136">Каждое значение также возвращается с идентификатором документа, имеющим значение Идрепресентативе.</span><span class="sxs-lookup"><span data-stu-id="c68fb-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="c68fb-137">SUM ( <column> )</span><span class="sxs-lookup"><span data-stu-id="c68fb-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="c68fb-138">Возвращает сумму значений в группе.</span><span class="sxs-lookup"><span data-stu-id="c68fb-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="c68fb-139">Применяется только к числам.</span><span class="sxs-lookup"><span data-stu-id="c68fb-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="c68fb-140">Статистические выражения возвращаются в виде отдельных столбцов.</span><span class="sxs-lookup"><span data-stu-id="c68fb-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="c68fb-141">Они являются главными простыми типами, за исключением Бифрекуенци, First, DateRange и Репресентативеоф, которые возвращаются как составные типы.</span><span class="sxs-lookup"><span data-stu-id="c68fb-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="c68fb-142">Для агрегатов можно использовать любой столбец числового значения или даты, а не только те, которые входят в предложение SELECT.</span><span class="sxs-lookup"><span data-stu-id="c68fb-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="c68fb-143">Однако нельзя группировать по статистическим выражениям.</span><span class="sxs-lookup"><span data-stu-id="c68fb-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="c68fb-144">Если переданный аргумент столбца не является числовым или типом даты, возвращается синтаксическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="c68fb-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="c68fb-145">Часть метки является необязательной и предоставляет более понятный псевдоним для метки.</span><span class="sxs-lookup"><span data-stu-id="c68fb-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="c68fb-146">Если вы не включили метку псевдонима, Поиск Windows преобразует функцию и имя столбца в метку.</span><span class="sxs-lookup"><span data-stu-id="c68fb-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="c68fb-147">Например, MAX (System.Docумент. WordCount) преобразуется в максимальное \_ системдокументвордкаунт.</span><span class="sxs-lookup"><span data-stu-id="c68fb-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="c68fb-148">Многоуровневые группы и подсчет</span><span class="sxs-lookup"><span data-stu-id="c68fb-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="c68fb-149">Агрегаты определяются над листьями и дублируются.</span><span class="sxs-lookup"><span data-stu-id="c68fb-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="c68fb-150">Статистическое выражение принимает в качестве входных данных конечные элементы группы, которая определяет ее (документы), а не подгруппы дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="c68fb-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="c68fb-151">Эта функция называется многоуровневой группировкой.</span><span class="sxs-lookup"><span data-stu-id="c68fb-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="c68fb-152">Помимо агрегатов, определяемых над листьями и повторяющимися, они считаются только один раз.</span><span class="sxs-lookup"><span data-stu-id="c68fb-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="c68fb-153">Хотя один и тот же документ может быть представлен несколько раз в одной группе, агрегаты будут рассматривать его только один раз.</span><span class="sxs-lookup"><span data-stu-id="c68fb-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="c68fb-154">Эта концепция показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="c68fb-154">The following graphic illustrates this concept.</span></span>

![Схема, показывающая, что агрегаты определены над листьями и повторяющимися и считаются только один раз](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="c68fb-156">Статистические примеры</span><span class="sxs-lookup"><span data-stu-id="c68fb-156">Aggregate Examples</span></span>

<span data-ttu-id="c68fb-157">Ниже приведены примеры агрегатных функций в предложении GROUP ON:</span><span class="sxs-lookup"><span data-stu-id="c68fb-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="c68fb-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c68fb-158">Return Value</span></span>

<span data-ttu-id="c68fb-159">Возвращаемое значение является вариантом, найденным в наборе строк как пользовательское свойство либо как заданные псевдонимы, либо как "агрегаты", если не указана метка псевдонима.</span><span class="sxs-lookup"><span data-stu-id="c68fb-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 




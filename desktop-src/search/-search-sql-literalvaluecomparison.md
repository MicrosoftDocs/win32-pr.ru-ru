---
description: При сравнении литеральных значений используются стандартные операторы сравнения для сопоставления однозначного столбца с литеральным значением.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Сравнение литеральных значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692188"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="01ef6-103">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="01ef6-103">Literal Value Comparison</span></span>

<span data-ttu-id="01ef6-104">При сравнении литеральных значений используются стандартные операторы сравнения для сопоставления однозначного столбца с [литеральным](-search-sql-literals.md) значением.</span><span class="sxs-lookup"><span data-stu-id="01ef6-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="01ef6-105">Дополнительные сведения о сравнении многозначных столбцов см. в разделе [сравнения с несколькими значениями (массивы)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="01ef6-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="01ef6-106">Предикат сравнения литеральных значений имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="01ef6-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="01ef6-107">Правая сторона сравнения должна быть литералом.</span><span class="sxs-lookup"><span data-stu-id="01ef6-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="01ef6-108">Невозможно сравнить столбец с вычисляемым значением и сравнить столбец с другим столбцом.</span><span class="sxs-lookup"><span data-stu-id="01ef6-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="01ef6-109">Часть столбца является допустимым столбцом свойств и при необходимости может быть приведена к другому типу.</span><span class="sxs-lookup"><span data-stu-id="01ef6-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="01ef6-110">При необходимости можно заключить имя столбца в двойные кавычки для удобочитаемости, не влияя на функциональность.</span><span class="sxs-lookup"><span data-stu-id="01ef6-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="01ef6-111">Дополнительные сведения см. [в разделе приведение типа данных столбца](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="01ef6-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="01ef6-112">Литерал может быть любым строковым, числовым, шестнадцатеричным, логическим или литералом даты, заключенным в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="01ef6-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="01ef6-113">Распознаются только точные соответствия, а подстановочные знаки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="01ef6-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="01ef6-114">Литерал также можно привести к другому типу.</span><span class="sxs-lookup"><span data-stu-id="01ef6-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="01ef6-115">Операторы сравнения</span><span class="sxs-lookup"><span data-stu-id="01ef6-115">Comparison Operators</span></span>

<span data-ttu-id="01ef6-116">В следующей таблице описаны поддерживаемые операторы сравнения.</span><span class="sxs-lookup"><span data-stu-id="01ef6-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="01ef6-117">Оператор сравнения</span><span class="sxs-lookup"><span data-stu-id="01ef6-117">Comparison operator</span></span> | <span data-ttu-id="01ef6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="01ef6-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="01ef6-119">Равно</span><span class="sxs-lookup"><span data-stu-id="01ef6-119">Equal to</span></span>                 |
| <span data-ttu-id="01ef6-120">! = или <></span><span class="sxs-lookup"><span data-stu-id="01ef6-120">!= or <></span></span>      | <span data-ttu-id="01ef6-121">Не равно</span><span class="sxs-lookup"><span data-stu-id="01ef6-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="01ef6-122">Больше</span><span class="sxs-lookup"><span data-stu-id="01ef6-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="01ef6-123">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="01ef6-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="01ef6-124">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="01ef6-124">Less than</span></span>                |
| <=               | <span data-ttu-id="01ef6-125">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="01ef6-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="01ef6-126">В сочетании с оператором "=" Windows Search язык SQL (SQL) поддерживает использование ключевых слов BEFORE и AFTER, которые указывают, должен ли запрос сравнивать значения столбцов до или после указанного значения в словаре сортировки словаря.</span><span class="sxs-lookup"><span data-stu-id="01ef6-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="01ef6-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="01ef6-127">Examples</span></span>

<span data-ttu-id="01ef6-128">Ниже приведены примеры предиката сравнения литеральных значений.</span><span class="sxs-lookup"><span data-stu-id="01ef6-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="01ef6-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01ef6-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="01ef6-130">**Reference**</span><span class="sxs-lookup"><span data-stu-id="01ef6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01ef6-131">Предикат LIKE</span><span class="sxs-lookup"><span data-stu-id="01ef6-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="01ef6-132">DATEADD, функция</span><span class="sxs-lookup"><span data-stu-id="01ef6-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="01ef6-133">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="01ef6-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="01ef6-134">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="01ef6-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="01ef6-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="01ef6-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="01ef6-136">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="01ef6-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="01ef6-137">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="01ef6-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




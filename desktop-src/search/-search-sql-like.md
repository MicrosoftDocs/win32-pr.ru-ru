---
description: Предикат LIKE выполняет сравнение сопоставления с шаблоном для указанного столбца.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Предикат LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719307"
---
# <a name="like-predicate"></a><span data-ttu-id="13fd7-103">Предикат LIKE</span><span class="sxs-lookup"><span data-stu-id="13fd7-103">LIKE Predicate</span></span>

<span data-ttu-id="13fd7-104">Предикат LIKE выполняет сравнение сопоставления с шаблоном для указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="13fd7-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="13fd7-105">Для этого используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="13fd7-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="13fd7-106"><column>Может быть обычным или иметь [идентификатор](-search-sql-identifiers.md)с разделителями.</span><span class="sxs-lookup"><span data-stu-id="13fd7-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="13fd7-107">Столбец ограничен свойствами в хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="13fd7-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="13fd7-108">> литерал с подстановочным знаком <\_ является строковым литералом.</span><span class="sxs-lookup"><span data-stu-id="13fd7-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="13fd7-109">Он заключается в кавычки и при необходимости может содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="13fd7-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="13fd7-110">При необходимости строка соответствия может содержать несколько подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="13fd7-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="13fd7-111">В следующей таблице описаны подстановочные знаки, распознаваемые предикатом LIKE.</span><span class="sxs-lookup"><span data-stu-id="13fd7-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="13fd7-112">Подстановочный знак</span><span class="sxs-lookup"><span data-stu-id="13fd7-112">Wildcard</span></span>                | <span data-ttu-id="13fd7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="13fd7-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="13fd7-114">Пример</span><span class="sxs-lookup"><span data-stu-id="13fd7-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fd7-115">% (в процентах)</span><span class="sxs-lookup"><span data-stu-id="13fd7-115">% (percent)</span></span>             | <span data-ttu-id="13fd7-116">Соответствует нулю или большему числу символов.</span><span class="sxs-lookup"><span data-stu-id="13fd7-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="13fd7-117">"comp% r" соответствует "Comp", за которой следует ноль или более символов, заканчивающихся на r.</span><span class="sxs-lookup"><span data-stu-id="13fd7-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="13fd7-118">\_ подчеркивания</span><span class="sxs-lookup"><span data-stu-id="13fd7-118">\_ (underscore)</span></span>         | <span data-ttu-id="13fd7-119">Соответствует любому отдельному символу.</span><span class="sxs-lookup"><span data-stu-id="13fd7-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="13fd7-120">"Comp \_ заве" соответствует "Comp", за которым следует только один символ, за которым следует "заве".</span><span class="sxs-lookup"><span data-stu-id="13fd7-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="13fd7-121">\[\](квадратные скобки)</span><span class="sxs-lookup"><span data-stu-id="13fd7-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="13fd7-122">Соответствует любому отдельному символу в указанном диапазоне или наборе.</span><span class="sxs-lookup"><span data-stu-id="13fd7-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="13fd7-123">Например, \[ a-z \] указывает диапазон; \[ AEIOU \] задает набор гласных.</span><span class="sxs-lookup"><span data-stu-id="13fd7-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="13fd7-124">"Comp \[ a-z \] Re" соответствует "Comp", за которым следует один символ в диапазоне от a до z, за которым следует ".</span><span class="sxs-lookup"><span data-stu-id="13fd7-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="13fd7-125">"Comp \[ AO \] " соответствует "Comp", за которым следует один символ, который должен быть либо a, либо o.</span><span class="sxs-lookup"><span data-stu-id="13fd7-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="13fd7-126">\[^ \] курсор</span><span class="sxs-lookup"><span data-stu-id="13fd7-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="13fd7-127">Соответствует любому отдельному символу, который не входит в указанный диапазон или набор.</span><span class="sxs-lookup"><span data-stu-id="13fd7-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="13fd7-128">Например, \[ ^ a-z \] указывает диапазон, исключающий от a до z; \[ ^ AEIOU \] указывает набор, исключающий гласные.</span><span class="sxs-lookup"><span data-stu-id="13fd7-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="13fd7-129">"Comp \[ ^ u \] " соответствует "Comp", за которым следует любой отдельный символ, отличный от u.</span><span class="sxs-lookup"><span data-stu-id="13fd7-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="13fd7-130">При создании предикатов с несколькими диапазонами диапазоны должны быть упорядочены по порядку.</span><span class="sxs-lookup"><span data-stu-id="13fd7-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="13fd7-131">Чтобы сопоставить символы-шаблоны как литеральные символы для сопоставления, а не в качестве подстановочных знаков, поместите символ в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="13fd7-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="13fd7-132">Например, чтобы сопоставить знак процента, используйте "". \[ % \]</span><span class="sxs-lookup"><span data-stu-id="13fd7-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="13fd7-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="13fd7-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="13fd7-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="13fd7-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="13fd7-135">**Reference**</span><span class="sxs-lookup"><span data-stu-id="13fd7-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13fd7-136">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="13fd7-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="13fd7-137">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="13fd7-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="13fd7-138">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="13fd7-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="13fd7-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="13fd7-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="13fd7-140">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="13fd7-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="13fd7-141">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="13fd7-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 





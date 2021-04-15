---
description: Условия, которые определяют, включен ли документ в результаты, возвращаемые запросом, указываются предложением WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Предложение WHERE (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682524"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="47fa8-103">Предложение WHERE (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="47fa8-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="47fa8-104">Условия, которые определяют, включен ли документ в результаты, возвращаемые запросом, указываются предложением WHERE.</span><span class="sxs-lookup"><span data-stu-id="47fa8-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="47fa8-105">На самом верхнем уровне синтаксис предложения WHERE состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="47fa8-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="47fa8-106">Необязательный псевдоним группы <\_> часть предложения упрощает сложные запросы путем назначения псевдонима группе из одного или нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="47fa8-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="47fa8-107">Это может улучшить удобочитаемость сложных запросов, которые выполняют поиск одной и той же информации в нескольких столбцах, указанных URL-адресами.</span><span class="sxs-lookup"><span data-stu-id="47fa8-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="47fa8-108">Дополнительные сведения о псевдонимах групп см. [в описании предиката AS Group Alias](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="47fa8-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="47fa8-109"><search condition>Часть предложения WHERE является одним или несколькими предикатами поиска, которые указывают условия поиска соответствия.</span><span class="sxs-lookup"><span data-stu-id="47fa8-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="47fa8-110">Предикаты поиска — это выражения, которые подтверждают некоторый факт о каком бы то ни было значении.</span><span class="sxs-lookup"><span data-stu-id="47fa8-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="47fa8-111">Результатом условия поиска является логическое значение, **true** , если документ соответствует указанным условиям поиска, или **false** , если нет.</span><span class="sxs-lookup"><span data-stu-id="47fa8-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="47fa8-112">Если результат равен **true**, возвращается документ.</span><span class="sxs-lookup"><span data-stu-id="47fa8-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="47fa8-113">Если результат равен **false**, документ не возвращается.</span><span class="sxs-lookup"><span data-stu-id="47fa8-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="47fa8-114">Документам, возвращаемым в запросе Microsoft Windows Search, присваиваются Ранжированные значения в соответствии с тем, насколько они соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="47fa8-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="47fa8-115">Каждое условие поиска запроса может включать предложение [ранкби](-search-sql-rankby.md) , которое поддерживает изменение возвращаемых значений ранга.</span><span class="sxs-lookup"><span data-stu-id="47fa8-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="47fa8-116">[Функция реусевхере](-search-sql-reusewhere.md) делает несколько запросов, использующих одни и те же условия поиска, более эффективными.</span><span class="sxs-lookup"><span data-stu-id="47fa8-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="47fa8-117">Предложение WHERE в запросе указывает набор элементов, соответствующих запросу.</span><span class="sxs-lookup"><span data-stu-id="47fa8-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="47fa8-118">Последующие запросы могут совместно использовать работу, выполненную для предыдущего евалутион, с помощью функции Реусевхере в предложении New запроса WHERE.</span><span class="sxs-lookup"><span data-stu-id="47fa8-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="47fa8-119">Поиск предикатов</span><span class="sxs-lookup"><span data-stu-id="47fa8-119">Search Predicates</span></span>

<span data-ttu-id="47fa8-120">Условие поиска состоит из одного или нескольких предикатов или условий поиска, описывающих, что пользователь ищет (например, если System. DateCreated > "2006-04-19").</span><span class="sxs-lookup"><span data-stu-id="47fa8-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="47fa8-121">Предикаты поиска можно комбинировать с помощью логических операторов **and** **, or или** **Not**.</span><span class="sxs-lookup"><span data-stu-id="47fa8-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="47fa8-122">Необязательный унарный оператор **Not** может использоваться только с **and** и только для отрицания логического значения предиката или условия поиска.</span><span class="sxs-lookup"><span data-stu-id="47fa8-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="47fa8-123">Круглые скобки можно использовать для группирования и вложения логических терминов.</span><span class="sxs-lookup"><span data-stu-id="47fa8-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="47fa8-124">В следующей таблице показан порядок приоритета для логических операторов.</span><span class="sxs-lookup"><span data-stu-id="47fa8-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="47fa8-125">Порядок (приоритет)</span><span class="sxs-lookup"><span data-stu-id="47fa8-125">Order (precedence)</span></span> | <span data-ttu-id="47fa8-126">Логический оператор</span><span class="sxs-lookup"><span data-stu-id="47fa8-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="47fa8-127">Первый (самый высокий)</span><span class="sxs-lookup"><span data-stu-id="47fa8-127">First (highest)</span></span>    | <span data-ttu-id="47fa8-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="47fa8-128">**NOT**</span></span>          |
| <span data-ttu-id="47fa8-129">Секунда</span><span class="sxs-lookup"><span data-stu-id="47fa8-129">Second</span></span>             | <span data-ttu-id="47fa8-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="47fa8-130">**AND**</span></span>          |
| <span data-ttu-id="47fa8-131">Третья (самая низкая)</span><span class="sxs-lookup"><span data-stu-id="47fa8-131">Third (lowest)</span></span>     | <span data-ttu-id="47fa8-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="47fa8-132">**OR**</span></span>           |



 

<span data-ttu-id="47fa8-133">Логические операторы одного и того же типа являются ассоциативными, и не существует заданного порядка вычисления.</span><span class="sxs-lookup"><span data-stu-id="47fa8-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="47fa8-134">Например, (A **и** B) **и** (C **и** d) можно вычислить (a **и** d) **и** (B **и** C) без изменения логического результата.</span><span class="sxs-lookup"><span data-stu-id="47fa8-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="47fa8-135">Неверно: где **не** содержит ("компьютер")</span><span class="sxs-lookup"><span data-stu-id="47fa8-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="47fa8-136">Верно: где CONTAINS (' программное обеспечение ') **и не** содержит (' Computer ')</span><span class="sxs-lookup"><span data-stu-id="47fa8-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="47fa8-137">В сложных запросах может потребоваться больше внимания на совпадениях в некоторых столбцах, чем в других.</span><span class="sxs-lookup"><span data-stu-id="47fa8-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="47fa8-138">Например, при поиске документов, в которых обсуждается «проектирование программного обеспечения», Поиск условия поиска в заголовке документа скорее всего будет хорошим совпадением, чем поиск отдельных слов в тексте документа.</span><span class="sxs-lookup"><span data-stu-id="47fa8-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="47fa8-139">Чтобы зависеть от ранжирования документов таким образом, язык запросов Microsoft Windows Search поддерживает взвешенные условия поиска.</span><span class="sxs-lookup"><span data-stu-id="47fa8-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="47fa8-140">Дополнительные сведения о взвешивании столбцов см. в разделе [Contains предикатов](-search-sql-contains.md) и [предиката FREETEXT](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="47fa8-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="47fa8-141">В поиске Windows есть три группы предикатов поиска: полнотекстовый, Неполнотекстовый, и поиск по глубине папок.</span><span class="sxs-lookup"><span data-stu-id="47fa8-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="47fa8-142">Предикаты полнотекстового поиска обычно соответствуют значению содержимого, заголовка и других столбцов и поддерживают лингвистическое сопоставление (например, альтернативные формы, фразы и поиск по сходству).</span><span class="sxs-lookup"><span data-stu-id="47fa8-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="47fa8-143">Напротив, предикаты, отличные от полнотекстового поиска, соответствуют значению указанных столбцов и не включают какую-либо специальную лингвистическую обработку, но в некоторых случаях предлагает сопоставление шаблонов на основе символов.</span><span class="sxs-lookup"><span data-stu-id="47fa8-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="47fa8-144">Предикаты глубины папок ограничивают область поиска указанным путем.</span><span class="sxs-lookup"><span data-stu-id="47fa8-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="47fa8-145">Если запрос возвращает документ, поскольку Неполнотекстовый предикат принимает значение **true** для этого документа, то значение Rank вычисляется как 1000.</span><span class="sxs-lookup"><span data-stu-id="47fa8-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="47fa8-146">С помощью [функции приведения рангов](-search-sql-rankby.md) можно изменить значение ранга.</span><span class="sxs-lookup"><span data-stu-id="47fa8-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="47fa8-147">В следующих таблицах описываются предикаты поиска полнотекстовых, неполнотекстовых и конечных папок.</span><span class="sxs-lookup"><span data-stu-id="47fa8-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="47fa8-148">Полнотекстовый предикат</span><span class="sxs-lookup"><span data-stu-id="47fa8-148">Full-text predicate</span></span>                  | <span data-ttu-id="47fa8-149">Description</span><span class="sxs-lookup"><span data-stu-id="47fa8-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47fa8-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="47fa8-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="47fa8-151">Поддерживает сложные поиски терминов в текстовых столбцах документа (например, Title, Content).</span><span class="sxs-lookup"><span data-stu-id="47fa8-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="47fa8-152">Может искать грамматические формы терминов поиска, проверять их сходство и выполнять логические сравнения.</span><span class="sxs-lookup"><span data-stu-id="47fa8-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="47fa8-153">Условия поиска могут содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="47fa8-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="47fa8-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="47fa8-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="47fa8-155">Выполняет поиск документов, соответствующих значению фразы поиска.</span><span class="sxs-lookup"><span data-stu-id="47fa8-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="47fa8-156">Связанные слова и похожие фразы будут соответствовать друг другу, а столбец Rank вычисляется в зависимости от того, насколько близко документ соответствует фразе поиска.</span><span class="sxs-lookup"><span data-stu-id="47fa8-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="47fa8-157">Условия поиска не могут содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="47fa8-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="47fa8-158">Неполнотекстовый предикат</span><span class="sxs-lookup"><span data-stu-id="47fa8-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="47fa8-159">Описание</span><span class="sxs-lookup"><span data-stu-id="47fa8-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47fa8-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="47fa8-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="47fa8-161">Значения столбцов сравниваются с помощью простого сопоставления шаблонов с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="47fa8-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="47fa8-162">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="47fa8-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="47fa8-163">Значения столбцов сравниваются со строками, датами, метками времени, числовыми значениями и другими литеральными значениями.</span><span class="sxs-lookup"><span data-stu-id="47fa8-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="47fa8-164">Этот предикат поддерживает равенство и неравенство, такие как «больше» и «меньше».</span><span class="sxs-lookup"><span data-stu-id="47fa8-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="47fa8-165">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="47fa8-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="47fa8-166">Многозначные столбцы сравниваются с многозначным массивом литералов.</span><span class="sxs-lookup"><span data-stu-id="47fa8-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="47fa8-167">NULL</span><span class="sxs-lookup"><span data-stu-id="47fa8-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="47fa8-168">Значения столбцов, которые не определены для документа, можно обнаружить с помощью предиката **null** .</span><span class="sxs-lookup"><span data-stu-id="47fa8-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="47fa8-169">Глубина папки</span><span class="sxs-lookup"><span data-stu-id="47fa8-169">Folder Depth</span></span>                             | <span data-ttu-id="47fa8-170">Описание</span><span class="sxs-lookup"><span data-stu-id="47fa8-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47fa8-171">КОТОРЫХ</span><span class="sxs-lookup"><span data-stu-id="47fa8-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="47fa8-172">Выполняет глубокий обход указанного пути, включая определенную папку и все вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="47fa8-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="47fa8-173">КАТАЛОГИ</span><span class="sxs-lookup"><span data-stu-id="47fa8-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="47fa8-174">Выполняет неполный обход указанного пути, выполняя поиск только указанной папки.</span><span class="sxs-lookup"><span data-stu-id="47fa8-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="47fa8-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="47fa8-175">Examples</span></span>

<span data-ttu-id="47fa8-176">Примеры предложения WHERE см. в разделах, посвященных отдельным предикатам, связанным в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="47fa8-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47fa8-177">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="47fa8-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="47fa8-178">**Reference**</span><span class="sxs-lookup"><span data-stu-id="47fa8-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="47fa8-179">Функция Реусевхере</span><span class="sxs-lookup"><span data-stu-id="47fa8-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="47fa8-180">Свойства набора строк</span><span class="sxs-lookup"><span data-stu-id="47fa8-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="47fa8-181">Предложение FROM</span><span class="sxs-lookup"><span data-stu-id="47fa8-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="47fa8-182">Общие сведения о синтаксисе SQL Search</span><span class="sxs-lookup"><span data-stu-id="47fa8-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="47fa8-183">С параметром--AS предикат псевдонима группы</span><span class="sxs-lookup"><span data-stu-id="47fa8-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="47fa8-184">Предикаты областей и каталогов</span><span class="sxs-lookup"><span data-stu-id="47fa8-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="47fa8-185">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="47fa8-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="47fa8-186">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="47fa8-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="47fa8-187">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="47fa8-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="47fa8-188">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="47fa8-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




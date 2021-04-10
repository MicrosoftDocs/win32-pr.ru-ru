---
description: Предикат CONTAINS является частью предложения WHERE и поддерживает поиск слов и фраз в текстовых столбцах.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Предикат CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896922"
---
# <a name="contains-predicate"></a><span data-ttu-id="cf645-103">Предикат CONTAINS</span><span class="sxs-lookup"><span data-stu-id="cf645-103">CONTAINS Predicate</span></span>

<span data-ttu-id="cf645-104">Предикат CONTAINS является частью предложения WHERE и поддерживает поиск слов и фраз в текстовых столбцах.</span><span class="sxs-lookup"><span data-stu-id="cf645-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="cf645-105">Предикат CONTAINS содержит функции для поиска совпадающих слов, соответствующие формы форм-слов, поиск с использованием подстановочных знаков и поиск по сходству.</span><span class="sxs-lookup"><span data-stu-id="cf645-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="cf645-106">Можно также применить весовые коэффициенты в предикате CONTAINS, чтобы задать важность столбцов, в которых найдено условие поиска.</span><span class="sxs-lookup"><span data-stu-id="cf645-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="cf645-107">Предикат CONTAINS лучше подходит для точных совпадений, в отличие от предиката [FREETEXT](-search-sql-freetext.md) , который лучше всего подходит для поиска документов, содержащих сочетания слов поиска, размещенных по всему столбцу.</span><span class="sxs-lookup"><span data-stu-id="cf645-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="cf645-108">Поиск выполняется без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="cf645-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="cf645-109">Ниже приведен базовый синтаксис предиката CONTAINS:</span><span class="sxs-lookup"><span data-stu-id="cf645-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="cf645-110">\_Ссылка на полнотекстовый столбец является необязательной.</span><span class="sxs-lookup"><span data-stu-id="cf645-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="cf645-111">С его помощью можно ограничить поиск одним столбцом или группой столбцов, в которой проверяется предикат CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="cf645-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="cf645-112">Если полнотекстовый столбец указан как "ALL" или " \* ", поиск выполняется по всем индексированным свойствам текста.</span><span class="sxs-lookup"><span data-stu-id="cf645-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="cf645-113">Хотя столбец не обязательно должен быть свойством Text, результаты могут быть бессмысленными, если столбец имеет другой тип данных.</span><span class="sxs-lookup"><span data-stu-id="cf645-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="cf645-114">Имя столбца может быть либо обычным, либо [идентификатором](-search-sql-identifiers.md)с разделителями, и его необходимо отделить от условия запятой.</span><span class="sxs-lookup"><span data-stu-id="cf645-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="cf645-115">Если полнотекстовый столбец не указан, используется столбец System. Search. Content, который является телом документа.</span><span class="sxs-lookup"><span data-stu-id="cf645-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="cf645-116">Часть LCID предиката указывает языковой стандарт поиска.</span><span class="sxs-lookup"><span data-stu-id="cf645-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="cf645-117">Это указывает поисковому механизму использовать соответствующие средства разбиения по словам и формы форм для поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="cf645-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="cf645-118">Чтобы указать языковой стандарт, укажите идентификатор кода языка Windows Standard (LCID).</span><span class="sxs-lookup"><span data-stu-id="cf645-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="cf645-119">Например, 1033 — это LCID для США-English.</span><span class="sxs-lookup"><span data-stu-id="cf645-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="cf645-120">Поместите LCID в качестве последнего элемента в скобках предложения CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="cf645-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="cf645-121">Важные сведения о поиске и языках см. [в разделе Использование локализованных поисков](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="cf645-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="cf645-122">По умолчанию в качестве языкового стандарта поиска используется системный язык по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf645-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="cf645-123">\_Часть условия Contains должна быть заключена в одинарные кавычки для отдельных слов или двойных кавычек для фраз и состоит из одного или нескольких терминов поиска содержимого, Объединенных с помощью логических операторов **и** или .</span><span class="sxs-lookup"><span data-stu-id="cf645-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="cf645-124">Необязательный унарный оператор можно использовать **не** после оператора **and** , чтобы инвертировать логическое значение условия поиска содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf645-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="cf645-125">Оператор **Not** может происходить только после **и**.</span><span class="sxs-lookup"><span data-stu-id="cf645-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="cf645-126">Нельзя использовать оператор **Not** , если имеется только одно условие соответствия или после оператора **or** .</span><span class="sxs-lookup"><span data-stu-id="cf645-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="cf645-127">Круглые скобки можно использовать для группирования и вложения условий поиска содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf645-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="cf645-128">В следующей таблице описывается порядок приоритета для логических операторов.</span><span class="sxs-lookup"><span data-stu-id="cf645-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="cf645-129">Порядок (приоритет)</span><span class="sxs-lookup"><span data-stu-id="cf645-129">Order (precedence)</span></span> | <span data-ttu-id="cf645-130">Логический оператор</span><span class="sxs-lookup"><span data-stu-id="cf645-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="cf645-131">Первый (самый высокий)</span><span class="sxs-lookup"><span data-stu-id="cf645-131">First (highest)</span></span>    | <span data-ttu-id="cf645-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="cf645-132">**NOT**</span></span>          |
| <span data-ttu-id="cf645-133">Секунда</span><span class="sxs-lookup"><span data-stu-id="cf645-133">Second</span></span>             | <span data-ttu-id="cf645-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="cf645-134">**AND**</span></span>          |
| <span data-ttu-id="cf645-135">Третья (самая низкая)</span><span class="sxs-lookup"><span data-stu-id="cf645-135">Third (lowest)</span></span>     | <span data-ttu-id="cf645-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="cf645-136">**OR**</span></span>           |

<span data-ttu-id="cf645-137">Логические операторы одного и того же типа являются ассоциативными, и не существует заданного порядка вычисления.</span><span class="sxs-lookup"><span data-stu-id="cf645-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="cf645-138">Например, (A **и** B) **и** (C **и** d) можно вычислить (B **и** C) **и** (A **и** d) без изменения логического результата.</span><span class="sxs-lookup"><span data-stu-id="cf645-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="cf645-139">В следующей таблице описаны типы условий поиска содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf645-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf645-140">Тип</span><span class="sxs-lookup"><span data-stu-id="cf645-140">Type</span></span></th>
<th><span data-ttu-id="cf645-141">Описание</span><span class="sxs-lookup"><span data-stu-id="cf645-141">Description</span></span></th>
<th><span data-ttu-id="cf645-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="cf645-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf645-143">Word</span><span class="sxs-lookup"><span data-stu-id="cf645-143">Word</span></span></td>
<td><span data-ttu-id="cf645-144">Одиночное слово без пробелов или других знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="cf645-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="cf645-145">Двойные кавычки не нужны.</span><span class="sxs-lookup"><span data-stu-id="cf645-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf645-146">Фраза</span><span class="sxs-lookup"><span data-stu-id="cf645-146">Phrase</span></span></td>
<td><span data-ttu-id="cf645-147">Несколько слов или вложенных пробелов.</span><span class="sxs-lookup"><span data-stu-id="cf645-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf645-148">Подстановочный знак</span><span class="sxs-lookup"><span data-stu-id="cf645-148">Wildcard</span></span></td>
<td><span data-ttu-id="cf645-149">Слова или фразы со звездочкой (\*), добавленной в конец.</span><span class="sxs-lookup"><span data-stu-id="cf645-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="cf645-150">Дополнительные сведения см. <a href="-search-sql-wildcards.md">в разделе Использование подстановочных знаков в предикате CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="cf645-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf645-151">Полнотекстовый столбец</span><span class="sxs-lookup"><span data-stu-id="cf645-151">Full-text Column</span></span></td>
<td><span data-ttu-id="cf645-152">Имя столбца свойств, по которому будет соответствовать оставшийся запрос.</span><span class="sxs-lookup"><span data-stu-id="cf645-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf645-153">Логическое</span><span class="sxs-lookup"><span data-stu-id="cf645-153">Boolean</span></span></td>
<td><span data-ttu-id="cf645-154">Слова, фразы и строки с подстановочными знаками, Объединенные с помощью логических операторов <strong>and</strong> <strong>, or</strong>или <strong>Not</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf645-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="cf645-155">Логические термины следует заключать в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="cf645-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf645-156">Near</span><span class="sxs-lookup"><span data-stu-id="cf645-156">Near</span></span></td>
<td><span data-ttu-id="cf645-157">Слова, фразы или подстановочные знаки, разделенные функцией NEAR.</span><span class="sxs-lookup"><span data-stu-id="cf645-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="cf645-158">Дополнительные сведения см. в разделе <a href="-search-sql-near.md">приближается к выражению</a>.</span><span class="sxs-lookup"><span data-stu-id="cf645-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf645-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="cf645-159">FormsOf</span></span></td>
<td><span data-ttu-id="cf645-160">Соответствует слову и версиям этого слова.</span><span class="sxs-lookup"><span data-stu-id="cf645-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="cf645-161">Дополнительные сведения см. в разделе <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span><span class="sxs-lookup"><span data-stu-id="cf645-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf645-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="cf645-162">IsAbout</span></span></td>
<td><span data-ttu-id="cf645-163">Объединяет совпадающие результаты по нескольким словам, фразам или условиям поиска с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="cf645-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="cf645-164">При необходимости каждое условие поиска может быть взвешенным.</span><span class="sxs-lookup"><span data-stu-id="cf645-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="cf645-165">При необходимости можно указать метод вычисления ранга, который сочетает весовые коэффициенты и количество элементов, соответствующих документу.</span><span class="sxs-lookup"><span data-stu-id="cf645-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="cf645-166">Дополнительные сведения см. в разделе <a href="-search-sql-isabout.md">о термине</a>.</span><span class="sxs-lookup"><span data-stu-id="cf645-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

<span data-ttu-id="cf645-167">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="cf645-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="cf645-168">Использование подстановочных знаков в предикате CONTAINS</span><span class="sxs-lookup"><span data-stu-id="cf645-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="cf645-169">FORMSOF термин</span><span class="sxs-lookup"><span data-stu-id="cf645-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="cf645-170">О термине</span><span class="sxs-lookup"><span data-stu-id="cf645-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="cf645-171">БЛИЖАЙШЕе условие</span><span class="sxs-lookup"><span data-stu-id="cf645-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="cf645-172">См. также</span><span class="sxs-lookup"><span data-stu-id="cf645-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="cf645-173">Справочник</span><span class="sxs-lookup"><span data-stu-id="cf645-173">Reference</span></span>

[<span data-ttu-id="cf645-174">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="cf645-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="cf645-175">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="cf645-175">Conceptual</span></span>

[<span data-ttu-id="cf645-176">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="cf645-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="cf645-177">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="cf645-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)

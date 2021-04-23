---
description: Группа в...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: ГРУППИРОВАТЬ ПО... ПОВЕРХ... Баланс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144089"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="79e0b-103">ГРУППИРОВАТЬ ПО... ПОВЕРХ... Баланс</span><span class="sxs-lookup"><span data-stu-id="79e0b-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="79e0b-104">Группа в... Поверх... Инструкция возвращает иерархический набор строк, в котором результаты поиска делятся на группы на основе указанного столбца и необязательных диапазонов группирования.</span><span class="sxs-lookup"><span data-stu-id="79e0b-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="79e0b-105">При группировке по столбцу [System. Kind](../properties/props-system-kind.md) результирующий набор делится на несколько групп: один для документов, один для обмена данными и т. д.</span><span class="sxs-lookup"><span data-stu-id="79e0b-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="79e0b-106">При группировании по [System. size](../properties/props-system-size.md) и group Range 100 КБ результирующий набор делится на три группы: элементы размером < 100 КБ, элементы размером >= 100 КБ и элементы без значения размера.</span><span class="sxs-lookup"><span data-stu-id="79e0b-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="79e0b-107">Можно также объединять группирования с функциями.</span><span class="sxs-lookup"><span data-stu-id="79e0b-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="79e0b-108">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="79e0b-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="79e0b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79e0b-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="79e0b-110">Диапазоны групп</span><span class="sxs-lookup"><span data-stu-id="79e0b-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="79e0b-111">Группы меток</span><span class="sxs-lookup"><span data-stu-id="79e0b-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="79e0b-112">Упорядочение групп</span><span class="sxs-lookup"><span data-stu-id="79e0b-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="79e0b-113">Вложенные группы</span><span class="sxs-lookup"><span data-stu-id="79e0b-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="79e0b-114">Группирование по свойствам вектора</span><span class="sxs-lookup"><span data-stu-id="79e0b-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="79e0b-115">Дополнительные примеры</span><span class="sxs-lookup"><span data-stu-id="79e0b-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="79e0b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="79e0b-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="79e0b-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79e0b-117">Syntax</span></span>

<span data-ttu-id="79e0b-118">Группа в... ПОВЕРХ... Инструкция имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="79e0b-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="79e0b-119">где диапазоны группирования определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="79e0b-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="79e0b-120">Группа по <column> может быть обычным или [идентификатором](-search-sql-identifiers.md) с разделителями для свойства в хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="79e0b-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="79e0b-121">Необязательный <group ranges> — это список из одного или нескольких значений (число, дата или строка), используемых для деления результатов на группы.</span><span class="sxs-lookup"><span data-stu-id="79e0b-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="79e0b-122"><range limit>Определяет точку деления в возвращенном результирующем наборе и <label> определяет понятную пользователю метку для группы.</span><span class="sxs-lookup"><span data-stu-id="79e0b-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="79e0b-123">Результирующий набор можно разделить на количество групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="79e0b-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="79e0b-124">Первая группа результатов включает элементы с минимально возможным значением для указанного свойства вплоть до, но не включая первый предел диапазона.</span><span class="sxs-lookup"><span data-stu-id="79e0b-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="79e0b-125">На эту группу можно ссылаться с помощью ключевого слова MINVALUE.</span><span class="sxs-lookup"><span data-stu-id="79e0b-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="79e0b-126">К второй группе можно обратиться как к самому спецификатору ограничения диапазона, так и к элементам, значение которых для указанного свойства больше или равно ограничению диапазона.</span><span class="sxs-lookup"><span data-stu-id="79e0b-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="79e0b-127">Все элементы, не имеющие значения для указанного свойства, возвращаются последними и могут называться ключевым словом **null** .</span><span class="sxs-lookup"><span data-stu-id="79e0b-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="79e0b-128">Например, ограничение диапазона, равное "2006-01-01" для свойства [System. DateCreated](../properties/props-system-datecreated.md) , делит результирующий набор на элементы с датами до 2006-01-01 (Группа MinValue), элементы с датами в или после 2006-01-01 (группа 2006-01-01) и элементы без даты (группа со **значением NULL** ).</span><span class="sxs-lookup"><span data-stu-id="79e0b-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="79e0b-129">В каждой группе результаты сортируются по значениям в столбце ГРУППИРОВАТЬ по по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79e0b-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="79e0b-130">Необязательное предложение [ORDER BY](-search-sql-orderby.md) может содержать описатель направления либо ASC для возрастания (с низким уровнем до высокого), либо DESC для нисходящего (от высокого до низкого), а предложение [Order в Group By](-search-sql-orderingroup.md) может упорядочивать каждую группу с помощью различных правил.</span><span class="sxs-lookup"><span data-stu-id="79e0b-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="79e0b-131">Дополнительные сведения см. в разделе [Упорядочение групп](#ordering-groups) ниже.</span><span class="sxs-lookup"><span data-stu-id="79e0b-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="79e0b-132">Диапазоны групп</span><span class="sxs-lookup"><span data-stu-id="79e0b-132">Group Ranges</span></span>

<span data-ttu-id="79e0b-133">В следующей таблице показано, как результаты делятся на группы на основе ограничений диапазона.</span><span class="sxs-lookup"><span data-stu-id="79e0b-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="79e0b-134">Пример ( <column> \[ диапазоны групп \] )</span><span class="sxs-lookup"><span data-stu-id="79e0b-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="79e0b-135">Результат</span><span class="sxs-lookup"><span data-stu-id="79e0b-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e0b-136">System. size \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="79e0b-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="79e0b-137">Результаты группируются в четыре сегмента: **MinValue**: Size < 1000</span><span class="sxs-lookup"><span data-stu-id="79e0b-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="79e0b-138">**1000:** 1000 <= размер < 5000</span><span class="sxs-lookup"><span data-stu-id="79e0b-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="79e0b-139">**5000:** Размер >= 5000</span><span class="sxs-lookup"><span data-stu-id="79e0b-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="79e0b-140">**Значение NULL:** Нет значения для размера</span><span class="sxs-lookup"><span data-stu-id="79e0b-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="79e0b-141">System. Author \[ до (m '), после (' r ')\]</span><span class="sxs-lookup"><span data-stu-id="79e0b-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="79e0b-142">Результаты группируются в четыре сегмента: **MinValue:** Author < символ перед "m"</span><span class="sxs-lookup"><span data-stu-id="79e0b-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="79e0b-143">**m:** символ перед "m" <= автор < символ после "r"</span><span class="sxs-lookup"><span data-stu-id="79e0b-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="79e0b-144">**r:** символ после "r" <= Author</span><span class="sxs-lookup"><span data-stu-id="79e0b-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="79e0b-145">**Значение NULL:** Нет значения для автора</span><span class="sxs-lookup"><span data-stu-id="79e0b-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="79e0b-146">System. Author \[ MinValue/' a to l ', ' m '/m-z '\]</span><span class="sxs-lookup"><span data-stu-id="79e0b-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="79e0b-147">Результаты группируются в три сегмента: **a в l:** Author < "m"</span><span class="sxs-lookup"><span data-stu-id="79e0b-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="79e0b-148">от **m до z:** "m" <= Author</span><span class="sxs-lookup"><span data-stu-id="79e0b-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="79e0b-149">**Значение NULL:** Нет значения для автора</span><span class="sxs-lookup"><span data-stu-id="79e0b-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="79e0b-150">System. DateCreated \[ ' 2005-1-01 ', ' 2006-6-01 '\]</span><span class="sxs-lookup"><span data-stu-id="79e0b-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="79e0b-151">Результаты группируются в четыре сегмента:</span><span class="sxs-lookup"><span data-stu-id="79e0b-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="79e0b-152">**MinValue:** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="79e0b-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="79e0b-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="79e0b-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="79e0b-154">**2006-1-01:** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="79e0b-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="79e0b-155">**Значение NULL:** Нет значения для DateCreated</span><span class="sxs-lookup"><span data-stu-id="79e0b-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="79e0b-156">Неверной `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="79e0b-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="79e0b-157">Правильно: `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="79e0b-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="79e0b-158">Группы меток</span><span class="sxs-lookup"><span data-stu-id="79e0b-158">Labeling Groups</span></span>

<span data-ttu-id="79e0b-159">Чтобы улучшить удобочитаемость, можно пометить группы с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="79e0b-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="79e0b-160">Метка отделяется от ограниченного диапазона символом косой черты и заключается в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="79e0b-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="79e0b-161">Если метка не указана, имя группы будет строкой ограничения диапазона.</span><span class="sxs-lookup"><span data-stu-id="79e0b-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="79e0b-162">Ниже приведен пример групп меток.</span><span class="sxs-lookup"><span data-stu-id="79e0b-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="79e0b-163">В Windows 7 или более поздней версии можно также использовать универсальную \[ другую \] метку для объединения нескольких диапазонов группирования.</span><span class="sxs-lookup"><span data-stu-id="79e0b-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="79e0b-164">Результаты из всех групп, указанных с помощью этой метки, будут объединены в одну группу с этой меткой.</span><span class="sxs-lookup"><span data-stu-id="79e0b-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="79e0b-165">Эта группа результатов возвращается после всех остальных групп, за исключением группы **со значением NULL** .</span><span class="sxs-lookup"><span data-stu-id="79e0b-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="79e0b-166">Группа **null** содержит результаты для элементов, которые не имеют значения для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="79e0b-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="79e0b-167">До Windows 7 \[ другая \] Метка рассматривается как любая другая метка группы.</span><span class="sxs-lookup"><span data-stu-id="79e0b-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="79e0b-168">Следующий код является примером использования \[ другой \] метки для групп, которые будут созданы в Windows 7 или более поздней версии:</span><span class="sxs-lookup"><span data-stu-id="79e0b-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="79e0b-169">В следующей таблице показаны группы, которые будут созданы с помощью предыдущего кода группирования в Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="79e0b-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="79e0b-170">Группа</span><span class="sxs-lookup"><span data-stu-id="79e0b-170">Group</span></span>     | <span data-ttu-id="79e0b-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="79e0b-171">System.Author</span></span> | <span data-ttu-id="79e0b-172">System. имя_файла</span><span class="sxs-lookup"><span data-stu-id="79e0b-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="79e0b-173">0</span><span class="sxs-lookup"><span data-stu-id="79e0b-173">0</span></span>         | <span data-ttu-id="79e0b-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="79e0b-174">1Bill</span></span>         | <span data-ttu-id="79e0b-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-175">Lorem.docx</span></span>      |
| <span data-ttu-id="79e0b-176">Q</span><span class="sxs-lookup"><span data-stu-id="79e0b-176">Q</span></span>         | <span data-ttu-id="79e0b-177">Дама</span><span class="sxs-lookup"><span data-stu-id="79e0b-177">Queen</span></span>         | <span data-ttu-id="79e0b-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="79e0b-179">Robin</span><span class="sxs-lookup"><span data-stu-id="79e0b-179">Robin</span></span>         | <span data-ttu-id="79e0b-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-180">dolor.docx</span></span>      |
| <span data-ttu-id="79e0b-181">Да</span><span class="sxs-lookup"><span data-stu-id="79e0b-181">Y</span></span>         | <span data-ttu-id="79e0b-182">зара</span><span class="sxs-lookup"><span data-stu-id="79e0b-182">Zara</span></span>          | <span data-ttu-id="79e0b-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-183">amet.docx</span></span>       |
| <span data-ttu-id="79e0b-184">\[ИНОЙ\]</span><span class="sxs-lookup"><span data-stu-id="79e0b-184">\[OTHER\]</span></span> | <span data-ttu-id="79e0b-185">абнер</span><span class="sxs-lookup"><span data-stu-id="79e0b-185">Abner</span></span>         | <span data-ttu-id="79e0b-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="79e0b-187">Владимир</span><span class="sxs-lookup"><span data-stu-id="79e0b-187">Bob</span></span>           | <span data-ttu-id="79e0b-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="79e0b-189">ксариа</span><span class="sxs-lookup"><span data-stu-id="79e0b-189">Xaria</span></span>         | <span data-ttu-id="79e0b-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-190">magna.docx</span></span>      |
| <span data-ttu-id="79e0b-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="79e0b-191">**NULL**</span></span>  |               | <span data-ttu-id="79e0b-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="79e0b-193">Упорядочение групп</span><span class="sxs-lookup"><span data-stu-id="79e0b-193">Ordering Groups</span></span>

<span data-ttu-id="79e0b-194">Существует три способа упорядочивания элементов в группах:</span><span class="sxs-lookup"><span data-stu-id="79e0b-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="79e0b-195">Порядок по умолчанию: если не указано иное, результаты упорядочиваются по значениям в столбце ГРУППИРОВАТЬ в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="79e0b-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="79e0b-196">ORDER BY: в предложении ORDER BY можно указать убывающий порядок.</span><span class="sxs-lookup"><span data-stu-id="79e0b-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="79e0b-197">Результаты необходимо упорядочить по столбцу GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="79e0b-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="79e0b-198">ПОРЯДОК в группе: можно указать другой порядок для каждой группы.</span><span class="sxs-lookup"><span data-stu-id="79e0b-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="79e0b-199">Если вы выполняете группировку по [System. Kind](../properties/props-system-kind.md), вы можете [](../properties/props-system-author.md) упорядочивать документы по System. Author [. исполнителя](../properties/props-system-music-artist.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="79e0b-200">Дополнительные сведения о сортировке результатов см. на страницах справочника [по предложениям ORDER BY](-search-sql-orderby.md) и [Order on Group](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="79e0b-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="79e0b-201">Вложенные группы</span><span class="sxs-lookup"><span data-stu-id="79e0b-201">Nesting Groups</span></span>

<span data-ttu-id="79e0b-202">Можно вкладывать группы с несколькими предложениями GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="79e0b-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="79e0b-203">Порядок, указанный в запросе, непосредственно отражается в иерархии выходных групп, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="79e0b-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="79e0b-204">System. Kind</span><span class="sxs-lookup"><span data-stu-id="79e0b-204">System.Kind</span></span>    | <span data-ttu-id="79e0b-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="79e0b-205">System.Author</span></span> | <span data-ttu-id="79e0b-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="79e0b-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="79e0b-207">документов</span><span class="sxs-lookup"><span data-stu-id="79e0b-207">documents</span></span>      | <span data-ttu-id="79e0b-208">вилла</span><span class="sxs-lookup"><span data-stu-id="79e0b-208">Willa</span></span>         | <span data-ttu-id="79e0b-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="79e0b-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="79e0b-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="79e0b-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="79e0b-211">зара</span><span class="sxs-lookup"><span data-stu-id="79e0b-211">Zara</span></span>          | <span data-ttu-id="79e0b-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="79e0b-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="79e0b-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="79e0b-213">2007-09-10</span></span>         |
| <span data-ttu-id="79e0b-214">IP-адресу (DIP)</span><span class="sxs-lookup"><span data-stu-id="79e0b-214">communications</span></span> | <span data-ttu-id="79e0b-215">абнер</span><span class="sxs-lookup"><span data-stu-id="79e0b-215">Abner</span></span>         | <span data-ttu-id="79e0b-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="79e0b-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="79e0b-217">Жан</span><span class="sxs-lookup"><span data-stu-id="79e0b-217">Jean</span></span>          | <span data-ttu-id="79e0b-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="79e0b-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="79e0b-219">вилла</span><span class="sxs-lookup"><span data-stu-id="79e0b-219">Willa</span></span>         | <span data-ttu-id="79e0b-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="79e0b-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="79e0b-221">зара</span><span class="sxs-lookup"><span data-stu-id="79e0b-221">Zara</span></span>          | <span data-ttu-id="79e0b-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="79e0b-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="79e0b-223">Группирование по свойствам вектора</span><span class="sxs-lookup"><span data-stu-id="79e0b-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="79e0b-224">Группирование по свойствам вектора, свойствам, которые могут содержать одно или несколько значений одновременно, по умолчанию сравнивает векторные значения по отдельности.</span><span class="sxs-lookup"><span data-stu-id="79e0b-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="79e0b-225">Например, если имеется один документ, Lorem.docx с свойством System. Author как «Сереса; Зара "и другой документ, Ipsum.docx с свойством System. Author как" Зара ", запрос возвращает результирующий набор в двух группах, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="79e0b-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="79e0b-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="79e0b-226">System.Author</span></span> | <span data-ttu-id="79e0b-227">System. имя_файла</span><span class="sxs-lookup"><span data-stu-id="79e0b-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="79e0b-228">сереса</span><span class="sxs-lookup"><span data-stu-id="79e0b-228">Theresa</span></span>       | <span data-ttu-id="79e0b-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-229">Lorem.docx</span></span>      |
| <span data-ttu-id="79e0b-230">зара</span><span class="sxs-lookup"><span data-stu-id="79e0b-230">Zara</span></span>          | <span data-ttu-id="79e0b-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="79e0b-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="79e0b-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="79e0b-233">Как видите, группирование по свойствам Vector возвращает дублирующиеся строки.</span><span class="sxs-lookup"><span data-stu-id="79e0b-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="79e0b-234">Lorem.docx появляется дважды, так как у него есть два автора.</span><span class="sxs-lookup"><span data-stu-id="79e0b-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="79e0b-235">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="79e0b-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="79e0b-236">См. также</span><span class="sxs-lookup"><span data-stu-id="79e0b-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e0b-237">Агрегатные функции</span><span class="sxs-lookup"><span data-stu-id="79e0b-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="79e0b-238">Предложение ORDER BY</span><span class="sxs-lookup"><span data-stu-id="79e0b-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="79e0b-239">ORDER в предложении GROUP</span><span class="sxs-lookup"><span data-stu-id="79e0b-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 

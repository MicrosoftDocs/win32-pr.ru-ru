---
description: Термин «о программе» сопоставляет столбцы с группой из одного или нескольких условий поиска.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: О термине
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808938"
---
# <a name="isabout-term"></a><span data-ttu-id="8040e-103">О термине</span><span class="sxs-lookup"><span data-stu-id="8040e-103">ISABOUT Term</span></span>

<span data-ttu-id="8040e-104">**Не рекомендуется**</span><span class="sxs-lookup"><span data-stu-id="8040e-104">**Deprecated**</span></span>

<span data-ttu-id="8040e-105">Эта функция была удалена в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8040e-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="8040e-106">При написании новых приложений Избегайте использования этой устаревшей функции.</span><span class="sxs-lookup"><span data-stu-id="8040e-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="8040e-107">При изменении существующих приложений настоятельно рекомендуется удалить все зависимости от этой функции.</span><span class="sxs-lookup"><span data-stu-id="8040e-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="8040e-108">Термин «о программе» сопоставляет столбцы с группой из одного или нескольких условий поиска.</span><span class="sxs-lookup"><span data-stu-id="8040e-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="8040e-109">Он имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8040e-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="8040e-110">Необязательный термин РАНКМЕСОД указывает метод вычисления, используемый для ранжирования документов, соответствующих одному или нескольким компонентам.</span><span class="sxs-lookup"><span data-stu-id="8040e-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="8040e-111">Если РАНКМЕСОД не указан, используется метод ранжирования Джаккарда коэффициента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8040e-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="8040e-112">Термин «о программе» может иметь один или несколько компонентов.</span><span class="sxs-lookup"><span data-stu-id="8040e-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="8040e-113">Столбцы, указанные в предикате [Contains](-search-sql-contains.md) , проверяются для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="8040e-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="8040e-114">Документ включается в результаты, если хотя бы один из компонентов соответствует.</span><span class="sxs-lookup"><span data-stu-id="8040e-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="8040e-115">Несколько компонентов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="8040e-115">Commas separate multiple components.</span></span>

<span data-ttu-id="8040e-116">Часть компонента имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8040e-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="8040e-117">Можно использовать необязательный термин веса для изменения относительной важности каждого термина в термине «о себе».</span><span class="sxs-lookup"><span data-stu-id="8040e-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="8040e-118">Если критерий веса не применяется, подразумевается вес 1,0 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8040e-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="8040e-119">В следующей таблице описаны возможные типы терминов соответствия.</span><span class="sxs-lookup"><span data-stu-id="8040e-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8040e-120">Тип</span><span class="sxs-lookup"><span data-stu-id="8040e-120">Type</span></span></th>
<th><span data-ttu-id="8040e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8040e-121">Description</span></span></th>
<th><span data-ttu-id="8040e-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="8040e-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8040e-123">Word</span><span class="sxs-lookup"><span data-stu-id="8040e-123">Word</span></span></td>
<td><span data-ttu-id="8040e-124">Одиночное слово без пробелов или других знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="8040e-124">A single word without spaces or other punctuation.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8040e-125">Фраза</span><span class="sxs-lookup"><span data-stu-id="8040e-125">Phrase</span></span></td>
<td><span data-ttu-id="8040e-126">Несколько слов или вложенных пробелов.</span><span class="sxs-lookup"><span data-stu-id="8040e-126">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8040e-127">Подстановочный знак</span><span class="sxs-lookup"><span data-stu-id="8040e-127">Wildcard</span></span></td>
<td><span data-ttu-id="8040e-128">Слова или фразы со звездочкой (\*), добавленной в конец.</span><span class="sxs-lookup"><span data-stu-id="8040e-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="8040e-129">Дополнительные сведения см. <a href="-search-sql-wildcards.md">в разделе Использование подстановочных знаков в предикате CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="8040e-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="8040e-130">О взвешивании столбцов</span><span class="sxs-lookup"><span data-stu-id="8040e-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="8040e-131">Термин «о программе» ранжирует совпадающие документы на основе того, насколько близко каждый документ соответствует набору условий соответствия в запросе.</span><span class="sxs-lookup"><span data-stu-id="8040e-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="8040e-132">Можно использовать весовые коэффициенты столбцов для повышения важности при совпадении с другими условиями соответствия.</span><span class="sxs-lookup"><span data-stu-id="8040e-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="8040e-133">Для каждого термина соответствия в термине «о себе» может быть применено весовое значение.</span><span class="sxs-lookup"><span data-stu-id="8040e-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="8040e-134">Весовой коэффициент применяется к одному выражению соответствия и указывается ключевым словом WEIGHT.</span><span class="sxs-lookup"><span data-stu-id="8040e-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="8040e-135">Выражение веса имеет два альтернативных синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="8040e-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="8040e-136">Значение веса должно находиться в диапазоне от 0 до 1,0 и содержать не более трех десятичных разрядов.</span><span class="sxs-lookup"><span data-stu-id="8040e-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="8040e-137">Указание весового значения вне этого диапазона приводит к появление сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8040e-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="8040e-138">Значение невзвешенного ранжирования для термина умножается на значение веса для этого термина.</span><span class="sxs-lookup"><span data-stu-id="8040e-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="8040e-139">Если для условия соответствия не указан вес, подразумевается значение по умолчанию 1,0.</span><span class="sxs-lookup"><span data-stu-id="8040e-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="8040e-140">Пример</span><span class="sxs-lookup"><span data-stu-id="8040e-140">Example</span></span>

<span data-ttu-id="8040e-141">В следующем примере весовые коэффициенты применяются к двум терминам соответствия, используя как длинный, так и короткий синтаксис для значений веса.</span><span class="sxs-lookup"><span data-stu-id="8040e-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="8040e-142">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8040e-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8040e-143">**Reference**</span><span class="sxs-lookup"><span data-stu-id="8040e-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8040e-144">Предикат FREETEXT</span><span class="sxs-lookup"><span data-stu-id="8040e-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="8040e-145">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="8040e-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 




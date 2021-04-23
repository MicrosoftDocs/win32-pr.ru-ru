---
description: Выражение NEAR используется для указания того, что два условия поиска содержимого должны быть относительно близко друг к другу, чтобы быть распознаны как совпадающие для предиката CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: БЛИЖАЙШЕе условие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342955"
---
# <a name="near-term"></a><span data-ttu-id="3309b-103">БЛИЖАЙШЕе условие</span><span class="sxs-lookup"><span data-stu-id="3309b-103">NEAR Term</span></span>

<span data-ttu-id="3309b-104">Выражение NEAR используется для указания того, что два условия поиска содержимого должны быть относительно близко друг к другу, чтобы быть распознаны как совпадающие для предиката [Contains](-search-sql-contains.md) .</span><span class="sxs-lookup"><span data-stu-id="3309b-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="3309b-105">Синтаксис БЛИЖАЙШИх терминов:</span><span class="sxs-lookup"><span data-stu-id="3309b-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="3309b-106">БЛИЖАЙШЕе выражение может быть представлено ключевым словом NEAR или тильдой (~).</span><span class="sxs-lookup"><span data-stu-id="3309b-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="3309b-107">Если слова, Соединенные NEAR в запросе, находятся в пределах приблизительно 50 слов друг от друга внутри искомого столбца, то выражение NEAR возвращает совпадение.</span><span class="sxs-lookup"><span data-stu-id="3309b-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="3309b-108">Чем ближе эти два слова, тем выше вычисленный рейтинг для БЛИЖАЙШЕГО термина.</span><span class="sxs-lookup"><span data-stu-id="3309b-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="3309b-109">Чем дальше два слова, тем меньше ранг.</span><span class="sxs-lookup"><span data-stu-id="3309b-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="3309b-110">Число слов между найденными поисковыми выражениями приблизительно и зависит от внешнего вида пропускаемых слов, таких как «a» или «The», а также от того, как разделители слов разбивают текст.</span><span class="sxs-lookup"><span data-stu-id="3309b-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="3309b-111">Это может быть менее 50.</span><span class="sxs-lookup"><span data-stu-id="3309b-111">It may be less than 50.</span></span>

 


<span data-ttu-id="3309b-112">В следующей таблице описаны типы терминов поиска содержимого, которые можно использовать с выражением NEAR в предикате CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="3309b-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3309b-113">Тип</span><span class="sxs-lookup"><span data-stu-id="3309b-113">Type</span></span></th>
<th><span data-ttu-id="3309b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3309b-114">Description</span></span></th>
<th><span data-ttu-id="3309b-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="3309b-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3309b-116">Word</span><span class="sxs-lookup"><span data-stu-id="3309b-116">Word</span></span></td>
<td><span data-ttu-id="3309b-117">Одиночное слово без пробелов или других знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="3309b-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="3309b-118">Двойные кавычки не нужны.</span><span class="sxs-lookup"><span data-stu-id="3309b-118">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3309b-119">Фраза</span><span class="sxs-lookup"><span data-stu-id="3309b-119">Phrase</span></span></td>
<td><span data-ttu-id="3309b-120">Несколько слов или вложенных пробелов.</span><span class="sxs-lookup"><span data-stu-id="3309b-120">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3309b-121">Подстановочный знак</span><span class="sxs-lookup"><span data-stu-id="3309b-121">Wildcard</span></span></td>
<td><span data-ttu-id="3309b-122">Слова или фразы со звездочкой (\*), добавленной в конец.</span><span class="sxs-lookup"><span data-stu-id="3309b-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="3309b-123">Дополнительные сведения см. <a href="-search-sql-wildcards.md">в разделе Использование подстановочных знаков в предикате CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="3309b-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="3309b-124">Если слова Match, указанные с ключевым словом NEAR, находятся в искомом столбце, но более чем на 50 слов, результат будет возвращен, но имеет [ранг](-search-sql-understandingrelevancevalues.md) 0.</span><span class="sxs-lookup"><span data-stu-id="3309b-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="3309b-125">Пример</span><span class="sxs-lookup"><span data-stu-id="3309b-125">Example</span></span>

<span data-ttu-id="3309b-126">В следующем примере показано связывание близких терминов с помощью коротких и длинных форм термина:</span><span class="sxs-lookup"><span data-stu-id="3309b-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="3309b-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3309b-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3309b-128">**Reference**</span><span class="sxs-lookup"><span data-stu-id="3309b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3309b-129">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="3309b-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="3309b-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3309b-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3309b-131">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="3309b-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="3309b-132">Использование подстановочных знаков в предикате CONTAINS</span><span class="sxs-lookup"><span data-stu-id="3309b-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 




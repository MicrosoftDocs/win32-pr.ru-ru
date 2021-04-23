---
description: Предикат FREETEXT является частью предложения WHERE и поддерживает поиск слов и фраз в текстовых столбцах.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Предикат FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808939"
---
# <a name="freetext-predicate"></a><span data-ttu-id="69528-103">Предикат FREETEXT</span><span class="sxs-lookup"><span data-stu-id="69528-103">FREETEXT Predicate</span></span>

<span data-ttu-id="69528-104">Предикат FREETEXT является частью предложения [WHERE](-search-sql-where.md) и поддерживает поиск слов и фраз в текстовых столбцах.</span><span class="sxs-lookup"><span data-stu-id="69528-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="69528-105">Используйте предикат FREETEXT для поиска документов, содержащих сочетания слов поиска, распределенных по заданному содержимому или столбцам.</span><span class="sxs-lookup"><span data-stu-id="69528-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="69528-106">Чтобы получить значение ранга, включите в качестве столбца в инструкции SELECT элемент System. Search. Rank, который является рангом релевенце.</span><span class="sxs-lookup"><span data-stu-id="69528-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="69528-107">Предикат FREETEXT имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="69528-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="69528-108">Ссылка на полнотекстовый столбец является необязательной.</span><span class="sxs-lookup"><span data-stu-id="69528-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="69528-109">С его помощью можно указать один столбец или [псевдоним группирования столбцов](-search-sql-with-as.md) , для которого проверяется предикат FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="69528-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="69528-110">Если полнотекстовый столбец указан как "ALL" или " \* ", поиск выполняется по всем индексированным свойствам текста.</span><span class="sxs-lookup"><span data-stu-id="69528-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="69528-111">Хотя столбец не обязательно должен быть свойством Text, результаты могут быть бессмысленными, если столбец имеет другой тип данных.</span><span class="sxs-lookup"><span data-stu-id="69528-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="69528-112">Имя столбца может быть либо обычным, либо [идентификатором](-search-sql-identifiers.md)с разделителями, и его необходимо отделить от условия запятой.</span><span class="sxs-lookup"><span data-stu-id="69528-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="69528-113">Если не указано полнотекстовое условие, используется столбец содержимого, который является телом документа.</span><span class="sxs-lookup"><span data-stu-id="69528-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="69528-114">Можно указать языковой стандарт поиска, чтобы определить подходящее средство разбиения по словам и формы форм для поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="69528-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="69528-115">Допустимые значения языкового стандарта — это идентификатор кода языка Windows Standard (LCID).</span><span class="sxs-lookup"><span data-stu-id="69528-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="69528-116">Например, 1033 — это LCID для США-English.</span><span class="sxs-lookup"><span data-stu-id="69528-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="69528-117">Поместите LCID в качестве последнего элемента в скобках предложения FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="69528-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="69528-118">Важные сведения о поиске и языках см. [в разделе Использование локализованных поисков](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="69528-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="69528-119">По умолчанию в качестве языкового стандарта поиска используется системный язык по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69528-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="69528-120">Часть условия FREETEXT необходимо заключить в одинарные кавычки, и она должна состоять из одного или нескольких условий поиска.</span><span class="sxs-lookup"><span data-stu-id="69528-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="69528-121">Предикат FREETEXT не поддерживает логические операции.</span><span class="sxs-lookup"><span data-stu-id="69528-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="69528-122">Чтобы найти фразу в виде одного слова, заключите эту фразу в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="69528-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="69528-123">При использовании предиката FREETEXT результаты запроса поиска возвращают документы, содержащие все условия поиска.</span><span class="sxs-lookup"><span data-stu-id="69528-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="69528-124">Условия не обязательно должны отображаться в каком бы то ни было определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="69528-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="69528-125">Документы, содержащие больше условий поиска, имеют более высокие значения столбцов ранга.</span><span class="sxs-lookup"><span data-stu-id="69528-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="69528-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="69528-126">Examples</span></span>

<span data-ttu-id="69528-127">В следующем примере выполняется поиск документов, содержащих "Computer", "Software", "Hardware" или сочетаний этих слов:</span><span class="sxs-lookup"><span data-stu-id="69528-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="69528-128">В одном предикате FREETEXT нельзя использовать как сопоставление одиночных слов, так и совпадение с фразой.</span><span class="sxs-lookup"><span data-stu-id="69528-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="69528-129">При выполнении запросов с контрактами кавычки необходимо заключать в контракт при использовании FREETEXT, но не при использовании ПРЕДИКАТа CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="69528-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="69528-130">Например, следующий синтаксис завершается ошибкой:</span><span class="sxs-lookup"><span data-stu-id="69528-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="69528-131">Правильный синтаксис включает в себя две одинарные кавычки, а не двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="69528-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="69528-132">Следующий синтаксис будет выполнен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="69528-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="69528-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="69528-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="69528-134">**Reference**</span><span class="sxs-lookup"><span data-stu-id="69528-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69528-135">Предикат CONTAINS</span><span class="sxs-lookup"><span data-stu-id="69528-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="69528-136">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="69528-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="69528-137">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="69528-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="69528-138">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="69528-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




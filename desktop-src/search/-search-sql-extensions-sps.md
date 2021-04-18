---
description: Microsoft Windows Search, основанный на стандартах SQL-92 и SQL-99, улучшает поиск на основе полнотекстовых документов в приложениях управления документами и управления знаниями.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Расширения SQL в Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540679"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="4db5c-103">Расширения SQL в Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="4db5c-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="4db5c-104">Microsoft Windows Search, основанный на стандартах SQL-92 и SQL-99, улучшает поиск на основе полнотекстовых документов в приложениях управления документами и управления знаниями.</span><span class="sxs-lookup"><span data-stu-id="4db5c-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="4db5c-105">Улучшения поиска Windows включают следующие:</span><span class="sxs-lookup"><span data-stu-id="4db5c-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="4db5c-106">128 — имена идентификаторов символов</span><span class="sxs-lookup"><span data-stu-id="4db5c-106">128-Character Identifier Names</span></span>

<span data-ttu-id="4db5c-107">Хотя SQL-92 и SQL-99 ограничивают столбец и другие идентификаторы до 18 символов, Поиск Windows поддерживает имена столбцов, сокоторые 128 символов.</span><span class="sxs-lookup"><span data-stu-id="4db5c-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="4db5c-108">Дополнительные сведения см. в статье [Идентификаторы](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="4db5c-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="4db5c-109">Группирование результатов по столбцам</span><span class="sxs-lookup"><span data-stu-id="4db5c-109">Grouping Results by Columns</span></span>

<span data-ttu-id="4db5c-110">Запросы могут указывать, как группировать результаты.</span><span class="sxs-lookup"><span data-stu-id="4db5c-110">Queries can specify how to group results.</span></span> <span data-ttu-id="4db5c-111">Можно указать диапазоны, по которым будет группироваться, и можно указать более одного столбца для группирования.</span><span class="sxs-lookup"><span data-stu-id="4db5c-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="4db5c-112">Например, можно группировать результаты по диапазонам размеров файлов (размер < 100, 100 <= размер < 1000; 1000 <= размер), а также вкладывать группы в вложенные.</span><span class="sxs-lookup"><span data-stu-id="4db5c-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="4db5c-113">Дополнительные сведения см [. в разделе Группирование по... Поверх... Оператор](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="4db5c-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="4db5c-114">Diacritic-Insensitive Поиск</span><span class="sxs-lookup"><span data-stu-id="4db5c-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="4db5c-115">Помимо поиска без учета регистра, Поиск Windows поддерживает поиск, не учитывающий диакритические знаки (диакритические знаки).</span><span class="sxs-lookup"><span data-stu-id="4db5c-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="4db5c-116">Дополнительные сведения см. [в разделе чувствительность к диакритическим знакам в поиске](-search-sql-accentinsensitivitysearches.md).</span><span class="sxs-lookup"><span data-stu-id="4db5c-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="4db5c-117">Взвешивание столбцов</span><span class="sxs-lookup"><span data-stu-id="4db5c-117">Column Weighting</span></span>

<span data-ttu-id="4db5c-118">Запросы, которые выполняют поиск более чем в одном столбце, могут указывать важность каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="4db5c-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="4db5c-119">Предикаты [Contains](-search-sql-contains.md) и [FREETEXT](-search-sql-freetext.md) поддерживают взвешивание столбцов.</span><span class="sxs-lookup"><span data-stu-id="4db5c-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="4db5c-120">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="4db5c-120">NULL Predicate</span></span>

<span data-ttu-id="4db5c-121">Хотя индексирование полнотекстового содержимого не имеет определенного набора столбцов, запросы могут требовать, чтобы элементы результирующего набора не имели определенных столбцов.</span><span class="sxs-lookup"><span data-stu-id="4db5c-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="4db5c-122">Невозможно различить документ с указанным свойством, значением которого является **null**, и документом, у которого нет свойства.</span><span class="sxs-lookup"><span data-stu-id="4db5c-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="4db5c-123">Изменение ранга</span><span class="sxs-lookup"><span data-stu-id="4db5c-123">Rank Modification</span></span>

<span data-ttu-id="4db5c-124">Ранжирование результатов поиска можно обрабатывать, используя [весовые коэффициенты](-search-sql-understandingrelevancevalues.md) для свойств и для групп свойств с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="4db5c-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="4db5c-125">Приведение рангов поддерживает прямую обработку ранжирования релевантности на основе указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="4db5c-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 




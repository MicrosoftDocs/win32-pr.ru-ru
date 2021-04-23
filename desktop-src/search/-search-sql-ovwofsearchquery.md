---
description: Язык SQL поиска Windows (SQL) аналогичен стандартному SQL-запросу.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Общие сведения о синтаксисе SQL для службы поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072645"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="88e73-103">Общие сведения о синтаксисе SQL для службы поиска Windows</span><span class="sxs-lookup"><span data-stu-id="88e73-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="88e73-104">Язык SQL поиска Windows (SQL) аналогичен стандартному SQL-запросу.</span><span class="sxs-lookup"><span data-stu-id="88e73-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="88e73-105">Он показан в следующих двух синтаксисах:</span><span class="sxs-lookup"><span data-stu-id="88e73-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="88e73-106">В следующем примере запроса возвращаются значения счетчика страниц и даты создания для всех документов, имеющих более 50 страниц, отсортированных в порядке возрастания количества страниц.</span><span class="sxs-lookup"><span data-stu-id="88e73-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="88e73-107">Синтаксис запроса Windows Search поддерживает множество вариантов, позволяющих выполнять более сложные запросы.</span><span class="sxs-lookup"><span data-stu-id="88e73-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="88e73-108">В следующей таблице описывается каждое предложение в инструкциях SELECT или GROUP ON и поддерживаемых функциях.</span><span class="sxs-lookup"><span data-stu-id="88e73-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="88e73-109">Предложение</span><span class="sxs-lookup"><span data-stu-id="88e73-109">Clause</span></span>                                              | <span data-ttu-id="88e73-110">Описание</span><span class="sxs-lookup"><span data-stu-id="88e73-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88e73-111">ГРУППИРОВАТЬ ПО... Поверх...</span><span class="sxs-lookup"><span data-stu-id="88e73-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="88e73-112">Задает способ группировки результатов, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="88e73-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="88e73-113">Можно указать диапазоны, по которым будет группироваться, и указать более одного столбца для группирования.</span><span class="sxs-lookup"><span data-stu-id="88e73-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="88e73-114">Например, можно группировать результаты по диапазонам размеров файлов (размер < 100, 100 <= размер < 1000; 1000 <= размер) и группировки вложений.</span><span class="sxs-lookup"><span data-stu-id="88e73-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="88e73-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="88e73-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="88e73-116">Указывает столбцы, возвращаемые запросом.</span><span class="sxs-lookup"><span data-stu-id="88e73-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="88e73-117">FROM</span><span class="sxs-lookup"><span data-stu-id="88e73-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="88e73-118">Указывает компьютер и каталог для поиска.</span><span class="sxs-lookup"><span data-stu-id="88e73-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="88e73-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="88e73-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="88e73-120">Указывает, что представляет собой соответствующий документ.</span><span class="sxs-lookup"><span data-stu-id="88e73-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="88e73-121">Это предложение имеет множество параметров, что позволяет управлять условиями поиска с широкими возможностями.</span><span class="sxs-lookup"><span data-stu-id="88e73-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="88e73-122">Например, можно сопоставлять слова, фразы, формы слов с формами, строки, числовые и битовые значения, а также многозначные массивы.</span><span class="sxs-lookup"><span data-stu-id="88e73-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="88e73-123">Можно также применить статистические веса к соответствующим условиям и объединить условия сопоставления с логическими операторами.</span><span class="sxs-lookup"><span data-stu-id="88e73-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="88e73-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="88e73-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="88e73-125">Задает порядок сортировки результатов, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="88e73-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="88e73-126">Можно указать несколько полей, по которым сортируются результаты, и можно использовать сортировку по возрастанию или по убыванию.</span><span class="sxs-lookup"><span data-stu-id="88e73-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="88e73-127">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="88e73-127">Code samples</span></span>

<span data-ttu-id="88e73-128">В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search через SQL.</span><span class="sxs-lookup"><span data-stu-id="88e73-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="88e73-129">В примере кода Всоледб показана библиотека ATL OLE DB доступ к приложениям поиска Windows, а также два дополнительных метода получения результатов из службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="88e73-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="88e73-130">Оба образца доступны на сайте [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="88e73-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e73-131">См. также</span><span class="sxs-lookup"><span data-stu-id="88e73-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="88e73-132">Справочник</span><span class="sxs-lookup"><span data-stu-id="88e73-132">Reference</span></span>

[<span data-ttu-id="88e73-133">Литералы</span><span class="sxs-lookup"><span data-stu-id="88e73-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="88e73-134">Использование локализованных поисков</span><span class="sxs-lookup"><span data-stu-id="88e73-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="88e73-135">Общие сведения о значимых значениях</span><span class="sxs-lookup"><span data-stu-id="88e73-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="88e73-136">Сопоставления свойств</span><span class="sxs-lookup"><span data-stu-id="88e73-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="88e73-137">Синтаксис расширенных запросов</span><span class="sxs-lookup"><span data-stu-id="88e73-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="88e73-138">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="88e73-138">Conceptual</span></span>

[<span data-ttu-id="88e73-139">Расширения SQL в Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="88e73-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="88e73-140">Функции SQL, недоступные в Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="88e73-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="88e73-141">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="88e73-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="88e73-142">Чувствительность к регистру при поиске</span><span class="sxs-lookup"><span data-stu-id="88e73-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="88e73-143">Чувствительность диакритических знаков в поиске</span><span class="sxs-lookup"><span data-stu-id="88e73-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="88e73-144">Приведение типа данных столбца</span><span class="sxs-lookup"><span data-stu-id="88e73-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="88e73-145">Сопоставления типов данных</span><span class="sxs-lookup"><span data-stu-id="88e73-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)

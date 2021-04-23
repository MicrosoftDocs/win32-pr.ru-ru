---
description: Язык запросов Microsoft Windows Search поддерживает шесть предикатов, не являющихся полнотекстовым поиском. Предикаты, описанные в этом разделе, перечислены в следующей таблице.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Неполнотекстовые предикаты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701388"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="c67b0-104">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="c67b0-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="c67b0-105">Язык запросов Microsoft Windows Search поддерживает шесть предикатов, не являющихся полнотекстовым поиском.</span><span class="sxs-lookup"><span data-stu-id="c67b0-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="c67b0-106">Предикаты, описанные в этом разделе, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c67b0-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="c67b0-107">Неполнотекстовый предикат</span><span class="sxs-lookup"><span data-stu-id="c67b0-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="c67b0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c67b0-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c67b0-109">ВСЕ побитовое и побитовое</span><span class="sxs-lookup"><span data-stu-id="c67b0-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="c67b0-110">— Это набор ключевых слов, посвященных проверке битов в целочисленном типе.</span><span class="sxs-lookup"><span data-stu-id="c67b0-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="c67b0-111">DATEADD, функция</span><span class="sxs-lookup"><span data-stu-id="c67b0-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="c67b0-112">Выполняет вычисления времени и даты для соответствующих свойств с типами дат.</span><span class="sxs-lookup"><span data-stu-id="c67b0-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="c67b0-113">Функция DATEADD используется для получения даты и времени в течение указанного промежутка времени до текущего.</span><span class="sxs-lookup"><span data-stu-id="c67b0-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="c67b0-114">Предикат LIKE</span><span class="sxs-lookup"><span data-stu-id="c67b0-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="c67b0-115">Сравнивает значения столбцов, используя простое сопоставление шаблонов с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="c67b0-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="c67b0-116">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="c67b0-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="c67b0-117">Сравнивает значения столбцов со строками, датами, метками времени, числовыми значениями и другими литеральными значениями.</span><span class="sxs-lookup"><span data-stu-id="c67b0-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="c67b0-118">Этот предикат поддерживает неравенство, например, больше (' > ') и меньше (' < ').</span><span class="sxs-lookup"><span data-stu-id="c67b0-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="c67b0-119">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="c67b0-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="c67b0-120">Сравнивает Многозначные столбцы с многозначным массивом литералов.</span><span class="sxs-lookup"><span data-stu-id="c67b0-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="c67b0-121">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="c67b0-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="c67b0-122">Обнаруживает значения столбцов, которые не определены для документа.</span><span class="sxs-lookup"><span data-stu-id="c67b0-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="c67b0-123">Поисковые запросы с помощью предиката **null** могут потребовать, чтобы поиск Windows проверял весь каталог, что может замедлить производительность запроса.</span><span class="sxs-lookup"><span data-stu-id="c67b0-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c67b0-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c67b0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c67b0-125">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="c67b0-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 




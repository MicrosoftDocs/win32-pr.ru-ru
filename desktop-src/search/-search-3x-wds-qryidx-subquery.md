---
description: Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Аргумент вложенного запроса (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990972"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="1f314-103">Аргумент вложенного запроса (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="1f314-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="1f314-104">Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="1f314-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="1f314-105">Результаты вложенного запроса используются в качестве источника для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="1f314-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="1f314-106">Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки электронной почты: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="1f314-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="1f314-107">Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.</span><span class="sxs-lookup"><span data-stu-id="1f314-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="1f314-108">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1f314-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1f314-109">Пример</span><span class="sxs-lookup"><span data-stu-id="1f314-109">Example</span></span>](#example)
-   [<span data-ttu-id="1f314-110">См. также</span><span class="sxs-lookup"><span data-stu-id="1f314-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="1f314-111">Пример</span><span class="sxs-lookup"><span data-stu-id="1f314-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="1f314-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1f314-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f314-113">Начало работы с Parameter-Valueными аргументами</span><span class="sxs-lookup"><span data-stu-id="1f314-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="1f314-114">Аргументы идентификатора языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="1f314-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="1f314-115">Переданный аргумент</span><span class="sxs-lookup"><span data-stu-id="1f314-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="1f314-116">Аргумент СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="1f314-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="1f314-117">СТАККЕДБИ, аргумент</span><span class="sxs-lookup"><span data-stu-id="1f314-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




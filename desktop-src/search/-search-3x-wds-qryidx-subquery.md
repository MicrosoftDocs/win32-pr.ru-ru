---
description: Сведения о аргументе вложенного запроса в Windows Search. Вложенный запрос — это сохраненный файл поиска, который можно использовать в качестве фильтра для нового запроса.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Аргумент вложенного запроса (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011037"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="e201e-104">Аргумент вложенного запроса (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="e201e-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="e201e-105">Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="e201e-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="e201e-106">Результаты вложенного запроса используются в качестве источника для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="e201e-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="e201e-107">Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки электронной почты: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="e201e-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="e201e-108">Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.</span><span class="sxs-lookup"><span data-stu-id="e201e-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="e201e-109">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e201e-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e201e-110">Пример</span><span class="sxs-lookup"><span data-stu-id="e201e-110">Example</span></span>](#example)
-   [<span data-ttu-id="e201e-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e201e-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="e201e-112">Пример</span><span class="sxs-lookup"><span data-stu-id="e201e-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="e201e-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e201e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e201e-114">Начало работы с Parameter-Valueными аргументами</span><span class="sxs-lookup"><span data-stu-id="e201e-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="e201e-115">Аргументы идентификатора языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="e201e-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="e201e-116">Переданный аргумент</span><span class="sxs-lookup"><span data-stu-id="e201e-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="e201e-117">Аргумент СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="e201e-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="e201e-118">СТАККЕДБИ, аргумент</span><span class="sxs-lookup"><span data-stu-id="e201e-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




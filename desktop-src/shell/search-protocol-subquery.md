---
description: Сведения о аргументе вложенного запроса в оболочке Windows. Вложенный запрос — это сохраненный файл поиска, который можно использовать в качестве фильтра для нового запроса.
title: Аргумент вложенного запроса (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010667"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="2a8e9-104">Аргумент вложенного запроса (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="2a8e9-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="2a8e9-105">Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="2a8e9-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="2a8e9-106">Результаты вложенного запроса используются в качестве источника для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="2a8e9-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="2a8e9-107">Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки по электронной почте: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="2a8e9-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="2a8e9-108">Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.</span><span class="sxs-lookup"><span data-stu-id="2a8e9-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="2a8e9-109">Пример</span><span class="sxs-lookup"><span data-stu-id="2a8e9-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="2a8e9-110">Сведения о аргументе</span><span class="sxs-lookup"><span data-stu-id="2a8e9-110">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="2a8e9-111">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="2a8e9-111">Minimum Operating System</span></span> | <span data-ttu-id="2a8e9-112">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="2a8e9-112">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 




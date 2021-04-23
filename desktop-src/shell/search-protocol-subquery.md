---
description: Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.
title: Аргумент вложенного запроса (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997886"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="24a6a-103">Аргумент вложенного запроса (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="24a6a-103">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="24a6a-104">Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="24a6a-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="24a6a-105">Результаты вложенного запроса используются в качестве источника для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="24a6a-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="24a6a-106">Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки по электронной почте: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS.</span><span class="sxs-lookup"><span data-stu-id="24a6a-106">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="24a6a-107">Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.</span><span class="sxs-lookup"><span data-stu-id="24a6a-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="24a6a-108">Например, .</span><span class="sxs-lookup"><span data-stu-id="24a6a-108">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="24a6a-109">Сведения о аргументе</span><span class="sxs-lookup"><span data-stu-id="24a6a-109">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="24a6a-110">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="24a6a-110">Minimum Operating System</span></span> | <span data-ttu-id="24a6a-111">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="24a6a-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 




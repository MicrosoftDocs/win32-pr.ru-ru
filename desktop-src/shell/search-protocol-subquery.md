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
# <a name="subquery-argument-the-windows-shell"></a>Аргумент вложенного запроса (оболочка Windows)

Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса. Результаты вложенного запроса используются в качестве источника для нового запроса. Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки по электронной почте: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS. Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.

## <a name="example"></a>Например, .


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Сведения о аргументе



|                          |                                         |
|--------------------------|-----------------------------------------|
| Минимальная операционная система | Windows Vista с пакетом обновления 1 (SP1) |



 

 

 




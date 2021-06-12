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
# <a name="subquery-argument-the-windows-shell"></a>Аргумент вложенного запроса (оболочка Windows)

Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса. Результаты вложенного запроса используются в качестве источника для нового запроса. Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки по электронной почте: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS. Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.

## <a name="example"></a>Пример


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Сведения о аргументе



|                          |                                         |
|--------------------------|-----------------------------------------|
| Минимальная операционная система | Windows Vista с пакетом обновления 1 (SP1) |



 

 

 




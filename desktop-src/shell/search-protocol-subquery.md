---
description: сведения о аргументе вложенного запроса в оболочке Windows. Вложенный запрос — это сохраненный файл поиска, который можно использовать в качестве фильтра для нового запроса.
title: аргумент вложенного запроса (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581602"
---
# <a name="subquery-argument-the-windows-shell"></a>аргумент вложенного запроса (оболочка Windows)

Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса. Результаты вложенного запроса используются в качестве источника для нового запроса. Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки по электронной почте: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS. Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.

## <a name="example"></a>Пример


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Сведения о аргументе



|                              | Значение                                   |
|------------------------------|-----------------------------------------|
| **Минимальная операционная система** | Windows Vista с пакетом обновления 1 (SP1) |



 

 

 




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
# <a name="subquery-argument-windows-search"></a>Аргумент вложенного запроса (Поиск Windows)

Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса. Результаты вложенного запроса используются в качестве источника для нового запроса. Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки электронной почты: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS. Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.

Этот раздел организован следующим образом:

-   [Пример](#example)
-   [См. также](#related-topics)

## <a name="example"></a>Пример


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Начало работы с Parameter-Valueными аргументами](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Аргументы идентификатора языкового стандарта](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Переданный аргумент](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Аргумент СИНТАКСИСа](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[СТАККЕДБИ, аргумент](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




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
# <a name="subquery-argument-windows-search"></a>Аргумент вложенного запроса (Поиск Windows)

Вложенный запрос — это сохраненный файл поиска ( \* . Search-MS), который можно использовать в качестве фильтра для нового запроса. Результаты вложенного запроса используются в качестве источника для нового запроса. Например, предположим, что имеется несколько сохраненных файлов поиска, ограничивающих запрос по списку рассылки электронной почты: мидепартмент. Search-MS, TeamProject. Search-MS и корпоратевиде. Search-MS. Использование `subquery` аргумента позволяет ограничить поиск по электронной почте любым из сохраненных поисков.

Этот раздел организован следующим образом:

-   [Пример](#example)
-   [Связанные темы](#related-topics)

## <a name="example"></a>Пример


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Связанные темы

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

 

 




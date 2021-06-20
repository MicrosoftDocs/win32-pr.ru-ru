---
description: Изучите аргументы инпутлокале и кэйвордлокале в Windows Search, которые помогают поисковой системе использовать правильные средства разбиения по словам.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Аргументы идентификатора локали (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403757"
---
# <a name="locale-identifier-arguments-windows-search"></a>Аргументы идентификатора локали (Поиск Windows)

`inputlocale` `keywordlocale` Идентификаторы и помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенного синтаксиса запросов. Это не всегда одинаковые идентификаторы кода языка (LCID), так как поиск Windows предлагается в нескольких международных версиях, а также включает пакеты MUI для других языков. Инпутлокале определяет код языка, на котором пользователи выполняют поисковый запрос в, а кэйвордлокале определяет код языка, используемый поисковой системой для ключевых слов.

Этот раздел организован следующим образом:

-   [Пример](#example)
-   [Связанные темы](#related-topics)

## <a name="example"></a>Пример


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Начало работы с Parameter-Valueными аргументами](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Переданный аргумент](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Аргумент СИНТАКСИСа](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[СТАККЕДБИ, аргумент](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Аргумент вложенного запроса](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 




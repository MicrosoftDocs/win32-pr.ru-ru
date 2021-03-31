---
description: Идентификаторы инпутлокале и кэйвордлокале помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенных синтаксисов запросов.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Аргументы идентификатора локали (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896949"
---
# <a name="locale-identifier-arguments-windows-search"></a>Аргументы идентификатора локали (Поиск Windows)

`inputlocale` `keywordlocale` Идентификаторы и помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенного синтаксиса запросов. Это не всегда одинаковые идентификаторы кода языка (LCID), так как поиск Windows предлагается в нескольких международных версиях, а также включает пакеты MUI для других языков. Инпутлокале определяет код языка, на котором пользователи выполняют поисковый запрос в, а кэйвордлокале определяет код языка, используемый поисковой системой для ключевых слов.

Этот раздел организован следующим образом:

-   [Пример](#example)
-   [См. также](#related-topics)

## <a name="example"></a>Пример


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>См. также

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

 

 




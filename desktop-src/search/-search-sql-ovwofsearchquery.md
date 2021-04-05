---
description: Язык SQL поиска Windows (SQL) аналогичен стандартному SQL-запросу.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Общие сведения о синтаксисе SQL для службы поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072645"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Общие сведения о синтаксисе SQL для службы поиска Windows

Язык SQL поиска Windows (SQL) аналогичен стандартному SQL-запросу. Он показан в следующих двух синтаксисах:


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

В следующем примере запроса возвращаются значения счетчика страниц и даты создания для всех документов, имеющих более 50 страниц, отсортированных в порядке возрастания количества страниц.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

Синтаксис запроса Windows Search поддерживает множество вариантов, позволяющих выполнять более сложные запросы.

В следующей таблице описывается каждое предложение в инструкциях SELECT или GROUP ON и поддерживаемых функциях.

| Предложение                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ГРУППИРОВАТЬ ПО... Поверх...](-search-sql-group-on-over.md) | Задает способ группировки результатов, возвращаемых запросом. Можно указать диапазоны, по которым будет группироваться, и указать более одного столбца для группирования. Например, можно группировать результаты по диапазонам размеров файлов (размер < 100, 100 <= размер < 1000; 1000 <= размер) и группировки вложений.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Указывает столбцы, возвращаемые запросом.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Указывает компьютер и каталог для поиска.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Указывает, что представляет собой соответствующий документ. Это предложение имеет множество параметров, что позволяет управлять условиями поиска с широкими возможностями. Например, можно сопоставлять слова, фразы, формы слов с формами, строки, числовые и битовые значения, а также многозначные массивы. Можно также применить статистические веса к соответствующим условиям и объединить условия сопоставления с логическими операторами. |
| [ORDER BY](-search-sql-orderby.md)                 | Задает порядок сортировки результатов, возвращаемых запросом. Можно указать несколько полей, по которым сортируются результаты, и можно использовать сортировку по возрастанию или по убыванию.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Примеры кода

В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search через SQL. В примере кода Всоледб показана библиотека ATL OLE DB доступ к приложениям поиска Windows, а также два дополнительных метода получения результатов из службы поиска Windows. Оба образца доступны на сайте [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[Литералы](-search-sql-literals.md)

[Использование локализованных поисков](-search-sql-usinglocsearches.md)

[Общие сведения о значимых значениях](-search-sql-understandingrelevancevalues.md)

[Сопоставления свойств](-search-3x-wds-propertymappings.md)

[Синтаксис расширенных запросов](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Основные понятия

[Расширения SQL в Microsoft Windows Search](-search-sql-extensions-sps.md)

[Функции SQL, недоступные в Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Идентификаторы](-search-sql-identifiers.md)

[Чувствительность к регистру при поиске](-search-sql-casesensitivityinsearches.md)

[Чувствительность диакритических знаков в поиске](-search-sql-accentinsensitivitysearches.md)

[Приведение типа данных столбца](-search-sql-castingdatacolumntype.md)

[Сопоставления типов данных](-search-sql-datatypemappings.md)

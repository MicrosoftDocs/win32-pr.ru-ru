---
description: При сравнении литеральных значений используются стандартные операторы сравнения для сопоставления однозначного столбца с литеральным значением.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Сравнение литеральных значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692188"
---
# <a name="literal-value-comparison"></a>Сравнение литеральных значений

При сравнении литеральных значений используются стандартные операторы сравнения для сопоставления однозначного столбца с [литеральным](-search-sql-literals.md) значением. Дополнительные сведения о сравнении многозначных столбцов см. в разделе [сравнения с несколькими значениями (массивы)](-search-sql-multivaluedcomparisons.md).

Предикат сравнения литеральных значений имеет следующий синтаксис:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Правая сторона сравнения должна быть литералом. Невозможно сравнить столбец с вычисляемым значением и сравнить столбец с другим столбцом.

 

Часть столбца является допустимым столбцом свойств и при необходимости может быть приведена к другому типу. При необходимости можно заключить имя столбца в двойные кавычки для удобочитаемости, не влияя на функциональность. Дополнительные сведения см. [в разделе приведение типа данных столбца](-search-sql-castingdatacolumntype.md).

Литерал может быть любым строковым, числовым, шестнадцатеричным, логическим или литералом даты, заключенным в одинарные кавычки. Распознаются только точные соответствия, а подстановочные знаки игнорируются. Литерал также можно привести к другому типу.

## <a name="comparison-operators"></a>Операторы сравнения

В следующей таблице описаны поддерживаемые операторы сравнения.



| Оператор сравнения | Описание              |
|---------------------|--------------------------|
| =                   | Равно                 |
| ! = или <>      | Не равно             |
| >                | Больше             |
| >=               | Больше или равно |
| <                | Меньше чем                |
| <=               | Меньше или равно    |



 

 

В сочетании с оператором "=" Windows Search язык SQL (SQL) поддерживает использование ключевых слов BEFORE и AFTER, которые указывают, должен ли запрос сравнивать значения столбцов до или после указанного значения в словаре сортировки словаря.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Примеры

Ниже приведены примеры предиката сравнения литеральных значений.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предикат LIKE](-search-sql-like.md)
</dt> <dt>

[DATEADD, функция](-search-sql-dateadd.md)
</dt> <dt>

[Сравнения с несколькими значениями (МАССИВы)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Предикат NULL](-search-sql-null.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Полнотекстовые предикаты](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Неполнотекстовые предикаты](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




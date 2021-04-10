---
description: Предикат CONTAINS является частью предложения WHERE и поддерживает поиск слов и фраз в текстовых столбцах.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Предикат CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896922"
---
# <a name="contains-predicate"></a>Предикат CONTAINS

Предикат CONTAINS является частью предложения WHERE и поддерживает поиск слов и фраз в текстовых столбцах. Предикат CONTAINS содержит функции для поиска совпадающих слов, соответствующие формы форм-слов, поиск с использованием подстановочных знаков и поиск по сходству. Можно также применить весовые коэффициенты в предикате CONTAINS, чтобы задать важность столбцов, в которых найдено условие поиска. Предикат CONTAINS лучше подходит для точных совпадений, в отличие от предиката [FREETEXT](-search-sql-freetext.md) , который лучше всего подходит для поиска документов, содержащих сочетания слов поиска, размещенных по всему столбцу. Поиск выполняется без учета регистра.

Ниже приведен базовый синтаксис предиката CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

\_Ссылка на полнотекстовый столбец является необязательной. С его помощью можно ограничить поиск одним столбцом или группой столбцов, в которой проверяется предикат CONTAINS. Если полнотекстовый столбец указан как "ALL" или " \* ", поиск выполняется по всем индексированным свойствам текста. Хотя столбец не обязательно должен быть свойством Text, результаты могут быть бессмысленными, если столбец имеет другой тип данных. Имя столбца может быть либо обычным, либо [идентификатором](-search-sql-identifiers.md)с разделителями, и его необходимо отделить от условия запятой. Если полнотекстовый столбец не указан, используется столбец System. Search. Content, который является телом документа.

Часть LCID предиката указывает языковой стандарт поиска. Это указывает поисковому механизму использовать соответствующие средства разбиения по словам и формы форм для поискового запроса. Чтобы указать языковой стандарт, укажите идентификатор кода языка Windows Standard (LCID). Например, 1033 — это LCID для США-English. Поместите LCID в качестве последнего элемента в скобках предложения CONTAINS. Важные сведения о поиске и языках см. [в разделе Использование локализованных поисков](-search-sql-usinglocsearches.md).

> [!NOTE]  
> По умолчанию в качестве языкового стандарта поиска используется системный язык по умолчанию.

\_Часть условия Contains должна быть заключена в одинарные кавычки для отдельных слов или двойных кавычек для фраз и состоит из одного или нескольких терминов поиска содержимого, Объединенных с помощью логических операторов **и** или . Необязательный унарный оператор можно использовать **не** после оператора **and** , чтобы инвертировать логическое значение условия поиска содержимого.

> [!NOTE]  
> Оператор **Not** может происходить только после **и**. Нельзя использовать оператор **Not** , если имеется только одно условие соответствия или после оператора **or** .

Круглые скобки можно использовать для группирования и вложения условий поиска содержимого. В следующей таблице описывается порядок приоритета для логических операторов.

| Порядок (приоритет) | Логический оператор |
|--------------------|------------------|
| Первый (самый высокий)    | **NOT**          |
| Секунда             | **AND**          |
| Третья (самая низкая)     | **OR**           |

Логические операторы одного и того же типа являются ассоциативными, и не существует заданного порядка вычисления. Например, (A **и** B) **и** (C **и** d) можно вычислить (B **и** C) **и** (A **и** d) без изменения логического результата.

В следующей таблице описаны типы условий поиска содержимого.

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип</th>
<th>Описание</th>
<th>Примеры</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Одиночное слово без пробелов или других знаков препинания. Двойные кавычки не нужны.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Фраза</td>
<td>Несколько слов или вложенных пробелов.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Подстановочный знак</td>
<td>Слова или фразы со звездочкой (*), добавленной в конец. Дополнительные сведения см. <a href="-search-sql-wildcards.md">в разделе Использование подстановочных знаков в предикате CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Полнотекстовый столбец</td>
<td>Имя столбца свойств, по которому будет соответствовать оставшийся запрос.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Логическое</td>
<td>Слова, фразы и строки с подстановочными знаками, Объединенные с помощью логических операторов <strong>and</strong> <strong>, or</strong>или <strong>Not</strong>. Логические термины следует заключать в двойные кавычки.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Near</td>
<td>Слова, фразы или подстановочные знаки, разделенные функцией NEAR. Дополнительные сведения см. в разделе <a href="-search-sql-near.md">приближается к выражению</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Соответствует слову и версиям этого слова. Дополнительные сведения см. в разделе <a href="-search-sql-formsof.md">FORMSOF Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Объединяет совпадающие результаты по нескольким словам, фразам или условиям поиска с подстановочными знаками. При необходимости каждое условие поиска может быть взвешенным. При необходимости можно указать метод вычисления ранга, который сочетает весовые коэффициенты и количество элементов, соответствующих документу. Дополнительные сведения см. в разделе <a href="-search-sql-isabout.md">о термине</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Этот раздел содержит следующие подразделы:

- [Использование подстановочных знаков в предикате CONTAINS](-search-sql-wildcards.md)
- [FORMSOF термин](-search-sql-formsof.md)
- [О термине](-search-sql-isabout.md)
- [БЛИЖАЙШЕе условие](-search-sql-near.md)

## <a name="related-topics"></a>См. также

### <a name="reference"></a>Справочник

[Предложения WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Основные понятия

[Полнотекстовые предикаты](-search-sql-fulltextpredicates.md)

[Неполнотекстовые предикаты](-search-sql-nonfulltextpredicates.md)

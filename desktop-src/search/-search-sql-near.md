---
description: Выражение NEAR используется для указания того, что два условия поиска содержимого должны быть относительно близко друг к другу, чтобы быть распознаны как совпадающие для предиката CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: БЛИЖАЙШЕе условие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342955"
---
# <a name="near-term"></a>БЛИЖАЙШЕе условие

Выражение NEAR используется для указания того, что два условия поиска содержимого должны быть относительно близко друг к другу, чтобы быть распознаны как совпадающие для предиката [Contains](-search-sql-contains.md) .

Синтаксис БЛИЖАЙШИх терминов:


```
<content_search_term> NEAR | ~ <content_search_term>
```



БЛИЖАЙШЕе выражение может быть представлено ключевым словом NEAR или тильдой (~).

Если слова, Соединенные NEAR в запросе, находятся в пределах приблизительно 50 слов друг от друга внутри искомого столбца, то выражение NEAR возвращает совпадение. Чем ближе эти два слова, тем выше вычисленный рейтинг для БЛИЖАЙШЕГО термина. Чем дальше два слова, тем меньше ранг.

> [!Note]  
> Число слов между найденными поисковыми выражениями приблизительно и зависит от внешнего вида пропускаемых слов, таких как «a» или «The», а также от того, как разделители слов разбивают текст. Это может быть менее 50.

 


В следующей таблице описаны типы терминов поиска содержимого, которые можно использовать с выражением NEAR в предикате CONTAINS.



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
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Если слова Match, указанные с ключевым словом NEAR, находятся в искомом столбце, но более чем на 50 слов, результат будет возвращен, но имеет [ранг](-search-sql-understandingrelevancevalues.md) 0.

 

### <a name="example"></a>Пример

В следующем примере показано связывание близких терминов с помощью коротких и длинных форм термина:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предложения WHERE](-search-sql-where.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Полнотекстовые предикаты](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Использование подстановочных знаков в предикате CONTAINS](-search-sql-wildcards.md)
</dt> </dl>

 

 




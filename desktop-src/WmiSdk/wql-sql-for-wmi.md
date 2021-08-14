---
description: язык запросов WMI (WQL) является подмножеством Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) &\# 8212; с незначительными семантическими изменениями. В следующей таблице перечислены ключевые слова WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9a1a3b0db3f383bd8ba44aeb1e433b5aab02b4e9b4773ea221e1a0254ae037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738823"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL WMI)

язык запросов WMI (WQL) — это подмножество Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) с незначительными семантическими изменениями. В следующей таблице перечислены ключевые слова WQL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ключевое слово WQL</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Объединяет два логических выражения и возвращает <strong>значение true</strong> , если оба выражения имеют <strong>значение true</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">СОЕДИНИТЕЛи</a></td>
<td>Извлекает все экземпляры, связанные с исходным экземпляром.<br/> Используйте эту инструкцию с запросами схемы и запросами данных.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Ссылается на класс объекта в запросе.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Указывает класс, содержащий свойства, перечисленные в инструкции SELECT. Windows Инструментарий управления (WMI) поддерживает запросы данных только из одного класса за раз.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Group, предложение</a></td>
<td>Заставляет Инструментарий WMI создать одно уведомление для представления группы событий.<br/> Используйте это предложение с запросами событий.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Фильтрует события, полученные в течение интервала группировки, указанного в <a href="within-clause.md">предложении Within</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Оператор сравнения, используемый с NOT и <strong>null</strong>. Для этой инструкции используется следующий синтаксис:<br/> ИМЕЕТ значение [NOT] <strong>null</strong><br/> (где не является обязательным)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Оператор, который применяет запрос к подклассам указанного класса. Дополнительные сведения см. в статьях <a href="isa-operator-for-event-queries.md">оператор ISA для запросов событий</a>, <a href="isa-operator-for-data-queries.md">оператор ISA для запросов данных</a>и <a href="isa-operator-for-schema-queries.md">оператор ISA для запросов схемы</a>.<br/></td>
</tr>
<tr class="odd">
<td>кэйсонли<br/></td>
<td>Используется в <a href="references-of-statement.md">ссылках</a> и <a href="associators-of-statement.md">связывающих</a> запросов, чтобы гарантировать, что результирующие экземпляры будут заполнены только ключами экземпляров, что снижает затраты на вызов.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Оператор, определяющий, совпадает ли данная символьная строка с указанным шаблоном.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Оператор сравнения, который используется в запросе WQL SELECT, например:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Указывает, что объект не имеет явно присвоенного значения. <strong>Значение NULL</strong> не эквивалентно нулю (0) или пусто.<br/></td>
</tr>
<tr class="odd">
<td>ИЛИ<br/></td>
<td>Объединяет два условия.<br/> Если в инструкции используется более одного логического оператора, то операторы или вычисляются после операторов и.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">ССЫЛКИ НА</a></td>
<td>Извлекает все экземпляры связей, ссылающиеся на конкретный экземпляр источника. Используйте эту инструкцию с запросами схемы и данных. <a href="references-of-statement.md">Ссылки</a> оператора похожи на операторы- <a href="associators-of-statement.md">соединители</a> оператора. Однако они не извлекают экземпляры конечных точек; Он извлекает экземпляры ассоциации.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Задает свойства, используемые в запросе.<br/> Дополнительные сведения см. в статьях <a href="select-statement-for-data-queries.md">инструкция SELECT для запросов данных</a>, <a href="select-statement-for-event-queries.md">инструкция SELECT для запросов событий</a>или <a href="select-statement-for-schema-queries.md">инструкция SELECT для запросов схемы</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Логический оператор, результатом вычисления которого является – 1 (минус единица).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Ограничивает область запроса данных, события или схемы.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Задает интервал опроса или группирования.<br/> Используйте это предложение с запросами событий.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Логический оператор, значением которого является 0 (ноль).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Использование ключевого слова WQL в качестве имени объекта может привести к созданию запроса, который не может быть проанализирован даже в случае, если запрос компилируется без ошибок.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Операторы WQL](wql-operators.md)
</dt> <dt>

[Форматы даты, поддерживаемые WQL](wql-supported-date-formats.md)
</dt> <dt>

[Поддерживаемые форматы времени WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 





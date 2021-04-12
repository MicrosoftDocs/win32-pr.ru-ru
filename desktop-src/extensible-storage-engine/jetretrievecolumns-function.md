---
description: Дополнительные сведения о функции Жетретриевеколумнс
title: Функция JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272393"
---
# <a name="jetretrievecolumns-function"></a>Функция JetRetrieveColumns


_**Применимо к:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>Функция JetRetrieveColumns

Функция **жетретриевеколумнс** получает несколько значений столбцов из текущей записи в одной операции. Массив структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) используется для описания набора значений столбцов для извлечения, а также для описания выходных буферов для каждого извлекаемого значения столбца.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*претриевеколумн*

Указатель на массив из одной или нескольких структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Каждая структура включает описание того, какое значение столбца необходимо извлечь и где хранить возвращенные данные.

*кретриевеколумн*

Число структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) в массиве, заданном параметром *претриевеколумн*.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence</p></td>
<td><p>Недопустимое значение порядкового номера столбца с несколькими значениями было передано в претинфо- &gt; итагсекуенце. Допустимые значения для порядковых номеров значений столбца с несколькими значениями: 1 или более. Значение 0 (ноль) допустимо для этой функции, но недопустимо для <a href="gg269198(v=exchg.10).md">жетретриевеколумн</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Столбцы, индексируемые как подстроки, не могут быть извлечены из индекса, так как в каждой записи индекса обычно содержится только небольшая часть столбца.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>В некоторых случаях буфер, заданный для столбца получения, должен иметь достаточный размер, чтобы вернуть любой объем значения столбца. Например, депонированные обновляемые столбцы настраиваются таким образом, чтобы они были согласованы в транзакционном контексте вызывающего сеанса, и эта корректировка требует наличия буфера, предоставленного вызывающим объектом. Если предоставлено недостаточное место в буфере, возвращается JET_errInvalidBufferSize и данные столбца не возвращаются.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один или несколько указанных параметров неверны. Это может произойти, если размер ретинфо. Кбструкт меньше, чем <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор не располагается на записи. Это может произойти по различным причинам. Например, это произойдет, если курсор находится в данный момент после последней записи в текущем индексе.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Не удалось получить значение полного столбца, так как размер данного буфера меньше размера столбца.</p></td>
</tr>
</tbody>
</table>


В случае успеха данные столбцов и размер столбца возвращаются в предоставленных буферах, описанных в разделе массив структур [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Если для *итагсекуенце* было задано значение 0 (ноль), чтобы указать, что вместо данных столбца требуется количество экземпляров многозначного поля, то число экземпляров многозначного столбца возвращается в самом поле *итагсекуенце* . Каждая структура [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) содержит поле ошибки, которое содержит предупреждения для извлекаемого столбца. Если столбец имеет **значение NULL** , то код ошибки будет установлен в JET_wrnColumnNull.

В случае сбоя положение курсора остается неизменным и данные не копируются в предоставленный буфер.

#### <a name="remarks"></a>Комментарии

**Жетретриевеколумнс** поддерживает одну функцию, которая не является [жетретриевеколумн](./jetretrievecolumn-function.md) . Это возможность получения количества экземпляров столбца с несколькими значениями. Эта функция предназначена для того, чтобы приложение получало все значения столбца. Это можно сделать, сначала определив количество значений в столбце. Затем их длину можно определить, вызвав **жетретриевеколумнс** еще раз с одной структурой [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) , выделенной для каждого значения, чтобы определить длину данных столбца. Это можно сделать, передав указатели **null**_пвдата_ с *кбмакс* 0 (нулем) и извлекая длину столбца в *кбактуал*. Третий и последний вызовы можно выполнить с выделенной памятью для данных значения столбца.

Если любой полученный столбец усекается из-за недостаточного размера буфера, API возвратит JET_wrnBufferTruncated. Однако другие ошибки, JET_wrnColumnNull возвращаются только в поле ошибки в [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Это связано с тем, что приложения часто хотят убедиться, что все данные получены и возвращать эту ошибку из **жетретриевеколумнс** , что упрощает это понимание.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[жетенумератеколумнс](./jetenumeratecolumns-function.md)  
[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетсетколумнс](./jetsetcolumns-function.md)

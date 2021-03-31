---
description: Дополнительные сведения о функции Жетопентабле
title: Функция JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808429"
---
# <a name="jetopentable-function"></a>Функция JetOpenTable


_**Применимо к:** Windows | Windows Server_

## <a name="jetopentable-function"></a>Функция JetOpenTable

Функция **жетопентабле** открывает курсор в ранее созданной таблице.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Используемый контекст сеанса базы данных.

*DBID*

Идентификатор базы данных, используемый для поиска таблицы.

*сзтабленаме*

Имя открываемой таблицы.

*пвпараметерс*

Не рекомендуется. Задайте **значение NULL**.

*кбпараметерс*

Не рекомендуется. Задайте значение 0 (ноль).

*грбит*

Группа битов, задающая ноль или более следующих параметров.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableDenyRead</p></td>
<td><p>Невозможно открыть таблицу для доступа на чтение в другом сеансе базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>Невозможно открыть таблицу для доступа на запись в другом сеансе базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>Не кэшировать страницы для этой таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Разрешает изменение DDL для таблиц, помеченных как Фикседддл. Этот параметр следует использовать с параметром JET_bitTableDenyRead.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Предоставляет указание о том, что таблица, вероятно, не находится в буферном кэше, и что предварительное чтение может быть полезно для повышения производительности.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Запрашивает доступ только для чтения к таблице.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>Таблица должна быть очень агрессивно выбиралась с диска, так как приложение будет сканировать его последовательно.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Запрашивает доступ на запись к таблице.</p></td>
</tr>
</tbody>
</table>


*pTableID*

При успешном выполнении указывает на идентификатор таблицы. При сбое содержимое для *pTableID* не определено.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>DBID</em> не является допустимым идентификатором базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Передано неправильное сочетание <em>грбит</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Имя, указанное в <em>сзтабленаме</em> , является недопустимым.</p>
<p>Дополнительные сведения о допустимых именах таблиц см. в описании параметра <em>сзтабленаме</em> в <a href="gg269210(v=exchg.10).md">жеткреатетабле</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Была предпринята попытка открыть таблицу, которая не существует в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора. См. раздел «Примечания».</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>Таблица используется другой операцией базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Некритическое предупреждение, указывающее, что таблица используется системой.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>Таблица заблокирована другой операцией базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Была предпринята попытка открыть слишком много уникальных таблиц одновременно. См. раздел «Примечания».</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Таблицы, открытые с помощью **жетопентабле** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md). Исключение из этого правила происходит при вызове **жетопентабле** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)). При откате транзакции таблица автоматически закрывается. В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).

Допустимо открывать системные таблицы с помощью **жетопентабле** (например, Мсисобжектс, мсисуникодефиксуп). Схема системных таблиц может измениться, поэтому доступ к системным таблицам не рекомендуется. Количество уникальных таблиц, которые могут быть открыты одновременно, повлияет непосредственно на *JET_paramMaxOpenTables*. Если таблица в данный момент открыта, в таблице будет создан новый курсор. Ресурсы курсора настраиваются с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с *JET_paramMaxCursors*. См. также [жетдупкурсор](./jetdupcursor-function.md).

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
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жетопентаблев</strong> (Юникод) и <strong>жетопентаблеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетдупкурсор](./jetdupcursor-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Параметры ресурсов](./resource-parameters.md)

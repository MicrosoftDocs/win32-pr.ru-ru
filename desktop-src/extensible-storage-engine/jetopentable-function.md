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
ms.openlocfilehash: 816bed58b4c886cc2e9984a44e1e4e10f7768f4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472528"
---
# <a name="jetopentable-function"></a>Функция JetOpenTable


_**Применимо к:** Windows | Windows Сервером_

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


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitTableDenyRead</p> | <p>Невозможно открыть таблицу для доступа на чтение в другом сеансе базы данных.</p> | 
| <p>JET_bitTableDenyWrite</p> | <p>Невозможно открыть таблицу для доступа на запись в другом сеансе базы данных.</p> | 
| <p>JET_bitTableNoCache</p> | <p>Не кэшировать страницы для этой таблицы.</p> | 
| <p>JET_bitTablePermitDDL</p> | <p>Разрешает изменение DDL для таблиц, помеченных как Фикседддл. Этот параметр следует использовать с параметром JET_bitTableDenyRead.</p> | 
| <p>JET_bitTablePreread</p> | <p>Предоставляет указание о том, что таблица, вероятно, не находится в буферном кэше, и что предварительное чтение может быть полезно для повышения производительности.</p> | 
| <p>JET_bitTableReadOnly</p> | <p>Запрашивает доступ только для чтения к таблице.</p> | 
| <p>JET_bitTableSequential</p> | <p>Таблица должна быть очень агрессивно выбиралась с диска, так как приложение будет сканировать его последовательно.</p> | 
| <p>JET_bitTableUpdatable</p> | <p>Запрашивает доступ на запись к таблице.</p> | 



*pTableID*

При успешном выполнении указывает на идентификатор таблицы. При сбое содержимое для *pTableID* не определено.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p><em>DBID</em> не является допустимым идентификатором базы данных.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Передано неправильное сочетание <em>грбит</em> .</p> | 
| <p>JET_errInvalidName</p> | <p>Имя, указанное в <em>сзтабленаме</em> , является недопустимым.</p><p>Дополнительные сведения о допустимых именах таблиц см. в описании параметра <em>сзтабленаме</em> в <a href="gg269210(v=exchg.10).md">жеткреатетабле</a>.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Была предпринята попытка открыть таблицу, которая не существует в базе данных.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора. См. раздел «Примечания».</p> | 
| <p>JET_errTableInUse</p> | <p>Таблица используется другой операцией базы данных.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Некритическое предупреждение, указывающее, что таблица используется системой.</p> | 
| <p>JET_errTableLocked</p> | <p>Таблица заблокирована другой операцией базы данных.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Была предпринята попытка открыть слишком много уникальных таблиц одновременно. См. раздел «Примечания».</p> | 



#### <a name="remarks"></a>Комментарии

Таблицы, открытые с помощью **жетопентабле** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md). Исключение из этого правила происходит при вызове **жетопентабле** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)). При откате транзакции таблица автоматически закрывается. В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).

Допустимо открывать системные таблицы с помощью **жетопентабле** (например, Мсисобжектс, мсисуникодефиксуп). Схема системных таблиц может измениться, поэтому доступ к системным таблицам не рекомендуется. Количество уникальных таблиц, которые могут быть открыты одновременно, повлияет непосредственно на *JET_paramMaxOpenTables*. Если таблица в данный момент открыта, в таблице будет создан новый курсор. Ресурсы курсора настраиваются с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с *JET_paramMaxCursors*. См. также [жетдупкурсор](./jetdupcursor-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетопентаблев</strong> (Юникод) и <strong>жетопентаблеа</strong> (ANSI).</p> | 



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

---
description: Дополнительные сведения о функции Жетопендатабасе
title: Функция JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819073"
---
# <a name="jetopendatabase-function"></a>Функция JetOpenDatabase


_**Применимо к:** Windows | Windows Server_

## <a name="jetopendatabase-function"></a>Функция JetOpenDatabase

Функция **жетопендатабасе** открывает ранее присоединенную базу данных с помощью функций [жетаттачдатабасе](./jetattachdatabase-function.md) или [JetAttachDatabase2](./jetattachdatabase2-function.md) для использования с сеансом базы данных. Эту функцию можно вызывать несколько раз для одной и той же базы данных.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя открываемой базы данных.

*сзконнект*

Зарезервировано. задано значение NULL.

*пдбид*

Указатель на буфер, который при успешном вызове содержит идентификатор базы данных. Если вызов завершается неудачно, значение не определено.

*грбит*

Группа битов, задающих ноль или более следующих параметров.

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
<td><p>JET_bitDbExclusive</p></td>
<td><p>Разрешает присоединение базы данных только одному сеансу. Как правило, база данных может быть открыта несколькими сеансами.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Предотвращает изменения в базе данных.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Был запрошен монопольный доступ, но его не удалось предоставить.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый файл.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Была предпринята попытка открыть несколько баз данных, а <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> были заданы. Дополнительные сведения см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>Файл был присоединен только для чтения, но <strong>жетопендатабасе</strong> не прошел JET_bitDbReadOnly. База данных по-прежнему открыта с доступом только для чтения.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Реализуется как <strong>жетопендатабасев</strong> (Юникод) и <strong>жетопендатабасеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)

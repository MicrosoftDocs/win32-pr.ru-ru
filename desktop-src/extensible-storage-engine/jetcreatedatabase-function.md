---
description: Дополнительные сведения о функции Жеткреатедатабасе
title: Функция JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358304"
---
# <a name="jetcreatedatabase-function"></a>Функция JetCreateDatabase


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetcreatedatabase-function"></a>Функция JetCreateDatabase

Функция **жеткреатедатабасе** создает и прикрепляет файл базы данных для использования с ЯДРОМ СУБД ESE. Вызов [JetCreateDatabase2](./jetcreatedatabase2-function.md) с *кпгдатабасесиземакс* , установленным в ноль, идентичен вызову **жеткреатедатабасе** с параметром *сзконнект* , имеющим значение null. В настоящее время для каждого экземпляра можно создать до семи баз данных.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя создаваемой базы данных.

*сзконнект*

Зарезервировано для последующего использования. задано значение NULL.

*пдбид*

Указатель на буфер, который при успешном вызове содержит идентификатор базы данных. При сбое значение не определено.

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
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>По умолчанию, если вызывается <strong>жеткреатедатабасе</strong> и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана. JET_bitDbOverwriteExisting изменяет это поведение, а старая база данных будет перезаписана новой. Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff отключает ведение журнала. Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после аварийного события.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>При установке JET_bitDbShadowingOff будет отключено дублирование некоторых внутренних структур баз данных (теневая). Дублирование этих структур выполняется для обеспечения устойчивости, поэтому параметр JET_bitDbShadowingOff удалит эту устойчивость.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>База данных с именем в <em>сзфиленаме</em> уже существует. При возвращении этой ошибки база данных не прикрепляется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Может возвращаться, если был запрошен монопольный доступ, но его не удалось предоставить, или если другой сеанс уже открыл базу данных в монопольном режиме.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Возвращается, если <em>кпгдатабасесиземакс</em> больше максимального числа страниц, разрешенного в базе данных. Текущее максимальное значение — 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> должен иметь значение, отличное от NULL. По умолчанию <em>сзфиленаме</em> должен указывать на существующий каталог. Путь будет создан, если задан параметр <em>JET_paramCreatePathIfNotExist</em> (см. <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Указывает, что другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Файл базы данных уже присоединен к другому сеансу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Предпринята попытка создать базу данных во время транзакции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Была предпринята попытка открыть несколько баз данных, а JET_paramOneDatabasePerSession были заданы. См. раздел <a href="gg269337(v=exchg.10).md">Параметры базы данных</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Не удалось выполнить операцию, так как не удалось выделить память.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>В каждом экземпляре может быть присоединено только конечное количество баз данных. Сейчас ограничение составляет семь баз данных на экземпляр.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly указывает, что файл был присоединен только для чтения, но <strong>жеткреатедатабасе</strong> не прошел JET_bitDbReadOnly. База данных по-прежнему открыта с доступом только для чтения.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Remarks

Если база данных, указанная в *сзфиленаме* , существует и JET_bitDbOverwriteExisting не была передана, вызов API завершится ошибкой. Если JET_bitDbOverwriteExisting был передан, старый файл базы данных будет удален первым.

Если API создает файл базы данных, а затем вызывает другую ошибку, он очищает и удаляет файл.

**Жеткреатедатабасе** будет неявно открывать базу данных. В дальнейшем не обязательно вызывать [жетопендатабасе](./jetopendatabase-function.md).

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
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
<td><p>Реализуется как <strong>жеткреатедатабасев</strong> (Юникод) и <strong>жеткреатедатабасеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также

[расширяемые файлы служба хранилища Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)

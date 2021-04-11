---
description: Дополнительные сведения о функции Жетаттачдатабасе
title: Функция JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262864"
---
# <a name="jetattachdatabase-function"></a>Функция JetAttachDatabase


_**Применимо к:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>Функция JetAttachDatabase

Функция **жетаттачдатабасе** присоединяет файл базы данных для использования с экземпляром базы данных. Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя присоединяемой базы данных.

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Если параметр <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> установлен, все индексы данных в Юникоде будут удалены. Дополнительные сведения см. в разделе "Примечания".</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Все индексы данных в Юникоде будут удалены независимо от значения параметра <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Дополнительные сведения см. в разделе "Примечания".</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Является устаревшей. Не используйте.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Присоединение базы данных во время резервного копирования не допускается.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Файл базы данных, указанный параметром <em>сзфиленаме</em> , должен быть доступным для записи. Атрибут Read-Only не должен быть задан, а выполняющийся процесс должен иметь достаточные привилегии для записи в файл.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Файл базы данных уже открыт другим процессом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый путь.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Файл базы данных уже присоединен к другому сеансу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Ядру СУБД не удается открыть файл базы данных. Возможно, файл используется другим процессом, или у вызывающего объекта недостаточно прав для открытия файла.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>Файл, указанный в <em>сзфиленаме</em> , не существует.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Ошибка в первичном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Она также может быть возвращена при присоединении базы данных, которая была изменена в более старой операционной системе, а первичный индекс — в столбце с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Ошибка в дополнительном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Он также может возвращаться при присоединении базы данных, которая была изменена в более старой версии операционной системы, а вторичный индекс — над столбцом с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания. Вторичные индексы полностью перестраиваются при дефрагментации базы данных с помощью автономной программы, используя следующую команду: <strong>Esentutl-d</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>В каждом экземпляре может быть присоединено только конечное число баз данных. Сейчас ограничение составляет семь баз данных на экземпляр.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Вызов **жетаттачдатабасе** эквивалентен вызову [JetAttachDatabase2](./jetattachdatabase2-function.md) и передаче нулевого значения, что означает отсутствие ограничения для параметра *кпгдатабасесиземакс* .

Присоединение базы данных, доступной для записи (то есть если JET_bitDbReadOnly не было указано в параметре *грбит* ), открывает файл исключительно на уровне операционной системы. Ни один другой процесс не сможет открыть файл. Несколько процессов могут присоединить одну базу данных, открыв их в режиме только для чтения.

Файл базы данных отсоединяется с помощью [жетдетачдатабасе](./jetdetachdatabase-function.md) или [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Параметры проверки индексов

Разные версии Windows вынормализуются текст в Юникоде различными способами. Это означает, что индексы, созданные в одной версии Windows, могут не работать в других версиях.

До Windows Server 2003 при изменении версии операционной системы (включая установку пакета обновления) каждый индекс данных в Юникоде находился в потенциально поврежденном состоянии.

Индексы, созданные в Windows Server 2003 и более поздних версий, помечаются версией нормализации Юникода, с которой они были построены. Более старые индексы не содержат сведений о версии. Большинство изменений нормализации Юникода состоит из добавления новых символов, а кодовые точки, которые ранее не были определены, теперь определяются и нормализуются по-разному. Таким образом, если двоичные данные хранятся в столбце в Юникоде, они будут по-разному нормализованы по мере определения новых кодовых точек.

Начиная с Windows Server 2003, ядро базы данных ESE отслеживает записи индекса в Юникоде, содержащие неопределенные кодовые точки. Их можно использовать для исправления индекса при изменении набора определенных символов Юникода.

Эти параметры управляют тем, что происходит, когда ядро базы данных ESE подключается к базе данных, которая была в последний раз использована в другой сборке операционной системы. Версия операционной системы отмечается в заголовке базы данных.

Если [JET_paramEnableIndexChecking](./database-parameters.md) имеет значение **true**, а база данных содержит потенциально поврежденные индексы:

  - **Жетаттачдатабасе** удалит потенциально поврежденные индексы, если *грбит* содержит JET_bitDbDeleteCorruptIndexes

  - **Жетаттачдатабасе** возвращает ошибку, если *грбит* не содержит JET_bitDbDeleteCorruptIndexes и есть индексы, которые требуется удалить.

Если [JET_paramEnableIndexChecking](./database-parameters.md) имеет значение **false**:

  - **Жетаттачдатабасе** пропускает потенциально поврежденные индексы и возвращает JET_errSuccess (при условии, что нет других ошибок).

Windows Server 2003 и более поздние версии: Если [JET_paramEnableIndexChecking](./database-parameters.md) не была сброшена, то для исправления записей индекса будет использоваться внутренняя таблица адресной привязки. Это может не исправить все повреждения индекса, но будет прозрачным для приложения.

Если база данных была подключена только для чтения, индекс не может быть исправлен или удален. В этом случае API возвратит ошибку, например JET_errSecondaryIndexCorrupted или JET_errPrimaryIndexCorrupted.

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
<td><p>Реализуется как <strong>жетаддколумнв</strong> (Юникод) и <strong>жетаддколумна</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[жетдетачдатабасе](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

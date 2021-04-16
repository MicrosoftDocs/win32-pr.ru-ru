---
description: Дополнительные сведения о функции JetAttachDatabase2
title: Функция JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712875"
---
# <a name="jetattachdatabase2-function"></a>Функция JetAttachDatabase2


_**Применимо к:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>Функция JetAttachDatabase2

Функция **JetAttachDatabase2** присоединяет файл базы данных для использования с экземпляром базы данных и задает максимальный размер для этой базы данных. Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, который будет использоваться для вызова API.

*сзфиленаме*

Имя присоединяемой базы данных.

*кпгдатабасесиземакс*

Максимальный размер (в страницах базы данных) для базы данных. Размер страницы базы данных по умолчанию — 4 килобайта, который можно изменить с помощью функции [жетсетсистемпараметер](./jetsetsystemparameter-function.md) перед созданием базы данных.

Передача нуля означает отсутствие ограничения, принудительно применяемого ядром СУБД.

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:

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
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Предотвращает изменения в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Функция возвращает один из [JET_ERR](./jet-err.md) кодов ошибок. Чаще всего возвращаются следующие. (Полный список ошибок для этого API см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).)

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
<td><p>JET_errFileNotFound</p></td>
<td><p>Файл, указанный в <em>сзфиленаме</em> , не существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Ошибка в первичном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Она также может быть возвращена при присоединении базы данных, которая была изменена в более старой операционной системе, а первичный индекс — в столбце с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Ошибка в дополнительном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Он также может возвращаться при присоединении базы данных, которая была изменена в более старой версии операционной системы, а вторичный индекс — над столбцом с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания. Вторичные индексы полностью перестраиваются при дефрагментации базы данных с помощью автономной программы, используя следующую команду: <strong>Esentutl-d</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>В каждом экземпляре может быть присоединено только конечное число баз данных. Сейчас ограничение составляет семь баз данных на экземпляр.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Файл базы данных отсоединяется с помощью [жетдетачдатабасе](./jetdetachdatabase-function.md) или [JetDetachDatabase2](./jetdetachdatabase2-function.md).

См. раздел [жетаттачдатабасе](./jetattachdatabase-function.md) for remarks.

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
<td><p>Реализуется как <strong>JetAttachDatabase2W</strong> (Юникод) и <strong>JetAttachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

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
ms.openlocfilehash: 069339aefbac335bf1c7bb4b35efe4466b526225
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475940"
---
# <a name="jetattachdatabase2-function"></a>Функция JetAttachDatabase2


_**Применимо к:** Windows | Windows Сервером_

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


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Если параметр <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> установлен, все индексы данных в Юникоде будут удалены. Дополнительные сведения см. в разделе "Примечания".</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Все индексы данных в Юникоде будут удалены независимо от значения параметра <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Дополнительные сведения см. в разделе "Примечания".</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Предотвращает изменения в базе данных.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Зарезервировано для последующего использования.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Функция возвращает один из [JET_ERR](./jet-err.md) кодов ошибок. Чаще всего возвращаются следующие. (полный список ошибок для этого API см. в разделе [коды ошибок расширенного обработчика служба хранилища](./extensible-storage-engine-error-codes.md).)


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Присоединение базы данных во время резервного копирования не допускается.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Файл базы данных, указанный параметром <em>сзфиленаме</em> , должен быть доступным для записи. Атрибут Read-Only не должен быть задан, а выполняющийся процесс должен иметь достаточные привилегии для записи в файл.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Файл базы данных уже открыт другим процессом.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый путь.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Файл базы данных уже присоединен к другому сеансу.</p> | 
| <p>JET_errFileNotFound</p> | <p>Файл, указанный в <em>сзфиленаме</em> , не существует.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Ошибка в первичном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Она также может быть возвращена при присоединении базы данных, которая была изменена в более старой операционной системе, а первичный индекс — в столбце с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Ошибка в дополнительном индексе. Это может быть из-за физического повреждения (например, повреждения диска или памяти). Он также может возвращаться при присоединении базы данных, которая была изменена в более старой версии операционной системы, а вторичный индекс — над столбцом с данными в Юникоде. Дополнительные сведения о индексах данных в Юникоде см. в разделе Примечания. Вторичные индексы полностью перестраиваются при дефрагментации базы данных с помощью автономной программы, используя следующую команду: <strong>Esentutl-d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>В каждом экземпляре может быть присоединено только конечное число баз данных. Сейчас ограничение составляет семь баз данных на экземпляр.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</p> | 



#### <a name="remarks"></a>Комментарии

Файл базы данных отсоединяется с помощью [жетдетачдатабасе](./jetdetachdatabase-function.md) или [JetDetachDatabase2](./jetdetachdatabase2-function.md).

См. раздел [жетаттачдатабасе](./jetattachdatabase-function.md) for remarks.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JetAttachDatabase2W</strong> (Юникод) и <strong>JetAttachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[расширяемые файлы служба хранилища Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

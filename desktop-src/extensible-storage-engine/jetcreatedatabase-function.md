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
ms.openlocfilehash: b7b3998d25d4f54d5150ad2a7a7d523f943d2eb7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465071"
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


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>По умолчанию, если вызывается <strong>жеткреатедатабасе</strong> и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана. JET_bitDbOverwriteExisting изменяет это поведение, а старая база данных будет перезаписана новой. Windows XP и более поздних версий.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff отключает ведение журнала. Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после аварийного события.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>При установке JET_bitDbShadowingOff будет отключено дублирование некоторых внутренних структур баз данных (теневая). Дублирование этих структур выполняется для обеспечения устойчивости, поэтому параметр JET_bitDbShadowingOff удалит эту устойчивость.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>База данных с именем в <em>сзфиленаме</em> уже существует. При возвращении этой ошибки база данных не прикрепляется.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Может возвращаться, если был запрошен монопольный доступ, но его не удалось предоставить, или если другой сеанс уже открыл базу данных в монопольном режиме.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Возвращается, если <em>кпгдатабасесиземакс</em> больше максимального числа страниц, разрешенного в базе данных. Текущее максимальное значение — 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> должен иметь значение, отличное от NULL. По умолчанию <em>сзфиленаме</em> должен указывать на существующий каталог. Путь будет создан, если задан параметр <em>JET_paramCreatePathIfNotExist</em> (см. <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Указывает, что другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Файл базы данных уже присоединен к другому сеансу.</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка создать базу данных во время транзакции.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Была предпринята попытка открыть несколько баз данных, а JET_paramOneDatabasePerSession были заданы. См. раздел <a href="gg269337(v=exchg.10).md">Параметры базы данных</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Не удалось выполнить операцию, так как не удалось выделить память.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>В каждом экземпляре может быть присоединено только конечное количество баз данных. Сейчас ограничение составляет семь баз данных на экземпляр.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Некритическое предупреждение, указывающее, что файл базы данных уже присоединен к этому сеансу.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly указывает, что файл был присоединен только для чтения, но <strong>жеткреатедатабасе</strong> не прошел JET_bitDbReadOnly. База данных по-прежнему открыта с доступом только для чтения.</p> | 



#### <a name="remarks"></a>Комментарии

Если база данных, указанная в *сзфиленаме* , существует и JET_bitDbOverwriteExisting не была передана, вызов API завершится ошибкой. Если JET_bitDbOverwriteExisting был передан, старый файл базы данных будет удален первым.

Если API создает файл базы данных, а затем вызывает другую ошибку, он очищает и удаляет файл.

**Жеткреатедатабасе** будет неявно открывать базу данных. В дальнейшем не обязательно вызывать [жетопендатабасе](./jetopendatabase-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жеткреатедатабасев</strong> (Юникод) и <strong>жеткреатедатабасеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

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

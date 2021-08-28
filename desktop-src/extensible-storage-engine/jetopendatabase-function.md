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
ms.openlocfilehash: 3fc7f484921dab0967ea991ac4060e5af7d78ec0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988499"
---
# <a name="jetopendatabase-function"></a>Функция JetOpenDatabase


_**Применимо к:** Windows | Windows Сервером_

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


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitDbExclusive</p> | <p>Разрешает присоединение базы данных только одному сеансу. Как правило, база данных может быть открыта несколькими сеансами.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Предотвращает изменения в базе данных.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Был запрошен монопольный доступ, но его не удалось предоставить.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>В <em>сзфиленаме</em>указан недопустимый путь. <em>сзфиленаме</em> не должно иметь значение NULL и ссылаться на допустимый файл.</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Другой сеанс уже открыл базу данных в монопольном режиме (с помощью JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a>).</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Предпринята попытка открыть файл, который не является допустимым файлом базы данных.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Была предпринята попытка открыть несколько баз данных, а <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> были заданы. Дополнительные сведения см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a>.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>Файл был присоединен только для чтения, но <strong>жетопендатабасе</strong> не прошел JET_bitDbReadOnly. База данных по-прежнему открыта с доступом только для чтения.</p> | 



#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетопендатабасев</strong> (Юникод) и <strong>жетопендатабасеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)

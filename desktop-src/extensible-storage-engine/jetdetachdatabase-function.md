---
description: Дополнительные сведения о функции Жетдетачдатабасе
title: Функция JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a66010b5d056301e368f7221380966adc2f31180
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470469"
---
# <a name="jetdetachdatabase-function"></a>Функция JetDetachDatabase


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdetachdatabase-function"></a>Функция JetDetachDatabase

Функция **жетдетачдатабасе** освобождает файл базы данных, который ранее был присоединен к сеансу базы данных.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя базы данных для отсоединения. Если *сзфиленаме* имеет **значение NULL** или является пустой строкой, все базы данных, прикрепленные к *сесид* , будут отсоединены.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBackupInProgress</p> | <p>База данных архивируется и не может быть отсоединена.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>База данных открыта с помощью <a href="gg269299(v=exchg.10).md">жетопендатабасе</a>. Перед отсоединением базы данных должны быть закрыты.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> или <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка отсоединить базу данных во время транзакции.</p> | 



#### <a name="remarks"></a>Комментарии

Если присоединенная база данных была открыта (с [жетаттачдатабасе](./jetattachdatabase-function.md)), ее необходимо закрыть с помощью [жетклоседатабасе](./jetclosedatabase-function.md) перед отсоединением.

только Windows 2000. базы данных, которые не были отсоединены до вызова [жеттерм](./jetterm-function.md) , будут автоматически присоединены при следующем вызове [жетинит](./jetinit-function.md) .

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетдетачдатабасев</strong> (Юникод) и <strong>жетдетачдатабасеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жеттерм](./jetterm-function.md)

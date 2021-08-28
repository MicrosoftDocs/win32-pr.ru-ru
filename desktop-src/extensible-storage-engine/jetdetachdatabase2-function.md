---
description: Дополнительные сведения о функции JetDetachDatabase2
title: Функция JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984887"
---
# <a name="jetdetachdatabase2-function"></a>Функция JetDetachDatabase2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdetachdatabase2-function"></a>Функция JetDetachDatabase2

Функция **JetDetachDatabase2** освобождает файл базы данных, который ранее был присоединен к сеансу базы данных.

**Windows xp:****JetDetachDatabase2** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя базы данных для отсоединения. Если *сзфиленаме* имеет **значение NULL** или является пустой строкой, все базы данных, прикрепленные к *сесид* , будут отсоединены.

*грбит*

Группа битов, задающая ноль или более следующих параметров.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Принудительное закрытие и отсоединение базы данных. Если JET_bitForceCloseAndDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</p> | 
| <p>JET_bitForceDetach</p> | <p>Принудительное отключение базы данных. Если JET_bitForceDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBackupInProgress</p> | <p>База данных архивируется и не может быть отсоединена.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>База данных открыта с помощью <a href="gg269299(v=exchg.10).md">жетопендатабасе</a>. Перед отсоединением базы данных должны быть закрыты.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> или <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach не поддерживается.</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка отсоединить базу данных во время транзакции.</p> | 



#### <a name="remarks"></a>Комментарии

Если присоединенная база данных была открыта (с [жетаттачдатабасе](./jetattachdatabase-function.md)), ее необходимо закрыть с помощью [жетклоседатабасе](./jetclosedatabase-function.md) перед отсоединением.

только Windows 2000. базы данных, которые не были отсоединены до вызова [жеттерм](./jetterm-function.md) , будут автоматически присоединены при следующем вызове [жетинит](./jetinit-function.md) .

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JetDetachDatabase2W</strong> (Юникод) и <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[жетинит](./jetinit-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жеттерм](./jetterm-function.md)

---
description: Дополнительные сведения о функции Жетделетеиндекс
title: Функция Жетделетеиндекс
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4170bd4def6ad60953189923252e2d775765b03d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478020"
---
# <a name="jetdeleteindex-function"></a>Функция Жетделетеиндекс


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdeleteindex-function"></a>Функция Жетделетеиндекс

Функция **жетделетеиндекс** Удаляет индекс из таблицы.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, содержащая удаляемый столбец.

*сзиндекснаме*

Имя удаляемого индекса.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errFixedDDL</p> | <p>Предпринята попытка удалить индекс из фиксированной таблицы (например, созданной с помощью JET_bitTableCreateFixedDDL).</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Предпринята попытка удалить индекс из таблицы шаблонов. Таблица шаблонов имеет фиксированное значение DDL.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Индекс с именем в <em>сзиндекснаме</em> не найден.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Невозможно обновить таблицу, так как она была открыта только для чтения.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Несколько потоков попытались использовать один сеанс базы данных.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Транзакция была открыта как транзакция только для чтения.</p> | 



#### <a name="remarks"></a>Комментарии

При успешном выполнении индекс удаляется, поэтому его нельзя использовать в дальнейшем. При использовании индекса не должно быть активной транзакции.

В случае успеха Валюта задается перед первой записью.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетделетеиндексв</strong> (Юникод) и <strong>жетделетеиндекса</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жеткреатеиндекс](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)

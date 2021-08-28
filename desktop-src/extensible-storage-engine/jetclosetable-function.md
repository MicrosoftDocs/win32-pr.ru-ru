---
description: Дополнительные сведения о функции Жетклосетабле
title: Функция Жетклосетабле
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe7f3c084a52faa9b5f011474bd0b502aebd277b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989067"
---
# <a name="jetclosetable-function"></a>Функция Жетклосетабле


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetclosetable-function"></a>Функция Жетклосетабле

Функция **жетклосетабле** закрывает открытую таблицу в базе данных. Таблица может быть временной или обычной таблицей.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Параметры

*сесид*

Определяет контекст сеанса базы данных, который будет использоваться для вызова API.

*TableID*

Определяет таблицу, которая должна быть закрыта.

Задайте для *tableid* значение JET_tableidNil, чтобы освободить память.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 



#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться для всех таблиц, открытых с помощью [жетопентабле](./jetopentable-function.md).

Исключение из этого правила происходит при вызове [жетопентабле](./jetopentable-function.md) в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)). При откате транзакции таблица автоматически закрывается. В этом случае возникает ошибка при закрытии таблицы с помощью **жетклосетабле**.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетопентабле](./jetopentable-function.md)  
[жетроллбакк](./jetrollback-function.md)

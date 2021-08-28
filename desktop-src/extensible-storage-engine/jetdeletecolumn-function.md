---
description: Дополнительные сведения о функции Жетделетеколумн
title: Функция Жетделетеколумн
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c7c73c5a6fd3249a8779526f6655992ad545372
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985917"
---
# <a name="jetdeletecolumn-function"></a>Функция Жетделетеколумн


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdeletecolumn-function"></a>Функция Жетделетеколумн

Функция **жетделетеколумн** удаляет столбец из таблицы базы данных ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, из которой необходимо удалить столбец.

*сзколумннаме*

Имя удаляемого столбца.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errColumnInUse</p> | <p>Столбец используется в данный момент. В настоящее время он может использоваться индексом.</p> | 
| <p>JET_errFixedDDL</p> | <p>Предпринята попытка изменить фиксированный DDL.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Столбец с именем в <em>сзколумннаме</em> существует в таблице шаблонов, а DDL таблицы шаблона изменить нельзя.</p> | 
| <p>JET_errInvalidName</p> | <p>Это может быть возвращено, если было задано неправильное имя <em>сзколумннаме</em> .</p> | 
| <p>JET_errPermissionDenied</p> | <p>Таблица недоступна для записи. Это может возвращаться, если база данных была открыта в режиме только для чтения.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Транзакция является транзакцией только для чтения.</p> | 



#### <a name="remarks"></a>Комментарии

Вызов **жетделетеколумн** идентичен вызову [JetDeleteColumn2](./jetdeletecolumn2-function.md) с параметром *грбит* , равным нулю (0).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетделетеколумнв</strong> (Юникод) и <strong>жетделетеколумна</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)

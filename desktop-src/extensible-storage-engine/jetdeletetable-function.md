---
description: Дополнительные сведения о функции Жетделететабле
title: Функция Жетделететабле
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984907"
---
# <a name="jetdeletetable-function"></a>Функция Жетделететабле


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdeletetable-function"></a>Функция Жетделететабле

Функция **жетделететабле** удаляет таблицу в базе данных ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*сзтабленаме*

Имя таблицы для удаления.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errTableInUse</p> | <p>Предпринята попытка удалить таблицу, в то время как другой сеанс имеет идентификатор открытой таблицы (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) с <a href="gg294118(v=exchg.10).md">жетопентабле</a> или <a href="gg269193(v=exchg.10).md">жетдупкурсор</a>.</p> | 
| <p>Таблица JET_errCannotDeletetemporary</p> | <p>Была предпринята попытка удалить временную таблицу. Временная таблица автоматически удаляется, когда она закрывается с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>Предпринята попытка удалить таблицу шаблонов, то есть таблицу, из которой может быть унаследована инструкция DDL.</p> | 



#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетделететаблев</strong> (Юникод) и <strong>жетделететаблеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[жетклосетабле](./jetclosetable-function.md)

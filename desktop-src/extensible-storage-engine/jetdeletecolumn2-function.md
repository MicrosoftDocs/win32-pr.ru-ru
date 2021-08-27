---
description: Дополнительные сведения о функции JetDeleteColumn2
title: Функция JetDeleteColumn2
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87e9506048094b77674e85f76f6c1718def44cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467171"
---
# <a name="jetdeletecolumn2-function"></a>Функция JetDeleteColumn2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdeletecolumn2-function"></a>Функция JetDeleteColumn2

Функция **JetDeleteColumn2** удаляет столбец из таблицы базы данных ESE и позволяет установить параметр *грбит* .

**Windows xp: JetDeleteColumn2** появился в Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, содержащая удаляемый столбец.

*сзколумннаме*

Имя удаляемого столбца.

*грбит*

Группа битов, задающая ноль или более следующих параметров.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>Установка JET_bitDeleteColumIgnoreTemplateColumns приведет к тому, что API будет пытаться только удалить столбцы в производной таблице. Если столбец с таким именем существует в базовой таблице, он будет проигнорирован.</p> | 



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

Вызов [жетделетеколумн](./jetdeletecolumn-function.md) идентичен вызову **JetDeleteColumn2** с параметром *грбит* , равным нулю (0).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JetDeleteColumn2W</strong> (Юникод) и <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетделетеколумн](./jetdeletecolumn-function.md)

---
description: Дополнительные сведения о функции Жеткреатеиндекс
title: Функция JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478400"
---
# <a name="jetcreateindex-function"></a>Функция JetCreateIndex


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetcreateindex-function"></a>Функция JetCreateIndex

функция **жеткреатеиндекс** позволяет создавать индексы данных служба хранилища в базе данных ESE, которая позволяет быстро находить нужные данные.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для конкретного вызова API.

*TableID*

Таблица, для которой будет создан индекс.

*сзиндекснаме*

Указатель на строку, завершающуюся нулем, которая указывает имя создаваемого индекса.

Имя индекса должно соответствовать следующим рекомендациям:

  - Оно должно содержать меньше символов, чем JET_cbNameMost, не включая завершающий символ null.

  - Он должен содержать только символы из следующих категорий: от 0 до 9, от A до Z, от a до z и всех знаков препинания, кроме " \! " (восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.

  - Оно не должно начинаться с пробела.

  - Он должен содержать по крайней мере один символ, не являющийся пробелом.

*грбит*

Группа битов, содержащая параметры, используемые для конкретного вызова. Этот параметр может содержать ноль или более параметров, найденных в структуре [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*сзкэй*

Указатель на строку, завершающуюся двойной нулем и заканчивающуюся токеном с разделителями null.

Дополнительные сведения об этом параметре см. в разделе Структура [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*cbKey*

Длина (в байтах) параметра *сзкэй* , включая два завершающих нуль символа.

*лденсити*

Процентная плотность начального дерева B +.

Дополнительные сведения об этом параметре см. в разделе Структура [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Значение</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 



Список дополнительных ошибок, которые могут возвращаться функцией **жеткреатеиндекс** , см. в разделе [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Комментарии

Вызов функции **жеткреатеиндекс** идентичен вызову функции [JetCreateIndex2](./jetcreateindex2-function.md) с структурой [JET_INDEXCREATE](./jet-indexcreate-structure.md) , содержащей те же параметры, что и параметры **жеткреатеиндекс**, и параметр *Циндекскреате* , равный 1. Для полей структуры [JET_INDEXCREATE](./jet-indexcreate-structure.md) , которые не имеют соответствующих параметров в **жеткреатеиндекс**, предполагается значение 0.

Обратите внимание, что **жеткреатеиндекс** был заменен [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Требования


| | | <p>Клиент</p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p>Сервер</p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p>Заголовок</p> | <p>Объявляется в ESENT. h.</p> | | <p>Библиотека</p> | <p>Использует ESENT. lib.</p> | | <p>DLL</p> | <p>Требуется ESENT.dll.</p> | | <p>Юникод</p> | <p>Реализуется как <strong>жеткреатеиндексв</strong> (Юникод) и <strong>жеткреатеиндекса</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)

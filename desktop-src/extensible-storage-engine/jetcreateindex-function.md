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
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712072"
---
# <a name="jetcreateindex-function"></a>Функция JetCreateIndex


_**Применимо к:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>Функция JetCreateIndex

Функция **жеткреатеиндекс** позволяет создавать индексы данных в базе данных ESE, которая позволяет быстро находить нужные данные.

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

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
</tbody>
</table>


Список дополнительных ошибок, которые могут возвращаться функцией **жеткреатеиндекс** , см. в разделе [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Комментарии

Вызов функции **жеткреатеиндекс** идентичен вызову функции [JetCreateIndex2](./jetcreateindex2-function.md) с структурой [JET_INDEXCREATE](./jet-indexcreate-structure.md) , содержащей те же параметры, что и параметры **жеткреатеиндекс**, и параметр *Циндекскреате* , равный 1. Для полей структуры [JET_INDEXCREATE](./jet-indexcreate-structure.md) , которые не имеют соответствующих параметров в **жеткреатеиндекс**, предполагается значение 0.

Обратите внимание, что **жеткреатеиндекс** был заменен [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Клиент</p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p>Сервер</p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td><p>Объявляется в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p>Библиотека</p></td>
<td><p>Использует ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Юникод</p></td>
<td><p>Реализуется как <strong>жеткреатеиндексв</strong> (Юникод) и <strong>жеткреатеиндекса</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)

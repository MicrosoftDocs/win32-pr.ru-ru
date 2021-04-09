---
description: Дополнительные сведения о функции Жетпререадиндексранжес
title: Функция Жетпререадиндексранжес
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143522"
---
# <a name="jetprereadindexranges-function"></a>Функция Жетпререадиндексранжес


_**Применимо к:** Windows | Windows Server_

Функция **жетпререадиндексранжес** считывает индексы для повышения производительности.

Функция **жетпререадиндексранжес** была введена в операционной системе Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, для которой выдаются сведения о предчтении.

*ргиндексранжес*

Диапазоны ключей для чтения.

*Циндексранжес*

Число диапазонов ключей для предчтения, определяемое числом элементов в *ргиндексранжес*.

*пкранжеспререад*

Количество диапазонов ключей, которые фактически были считаны.

*ргколумнидпререад*

Список идентификаторов столбцов для столбцов с длинными значениями для чтения. По умолчанию предварительно считывается только запись на странице. Если необходимо предварительно прочитать столбцы с длинными значениями в виде страниц, их идентификаторы столбцов должны передаваться через этот параметр.

*кколумнидпререад*

Количество идентификаторов столбцов для столбцов с длинными значениями, которые должны быть считаны, определяется числом элементов в *ргколумнидпререад*.

*грбит*

Группа битов, указывающая ноль или более значений направления, перечисленных в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Вперед</p></td>
<td><p>Чтение вперед.</p></td>
</tr>
<tr class="even">
<td><p>Назад</p></td>
<td><p>Прочтите обратно.</p></td>
</tr>
<tr class="odd">
<td><p>фирстпажеонли</p></td>
<td><p>Предварительное чтение только первой страницы любого столбца Long.</p></td>
</tr>
<tr class="even">
<td><p>нормализедкэй</p></td>
<td><p>Нормализованное значение ключа или закладки вместо значения столбца.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, следует запустить асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также раздел

[JET_ERR](./jet-err.md)

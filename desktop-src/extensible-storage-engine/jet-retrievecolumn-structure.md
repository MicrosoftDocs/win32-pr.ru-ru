---
description: 'Дополнительные сведения: структура JET_RETRIEVECOLUMN'
title: Структура JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701663"
---
# <a name="jet_retrievecolumn-structure"></a>Структура JET_RETRIEVECOLUMN


_**Применимо к:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>Структура JET_RETRIEVECOLUMN

Структура **JET_RETRIEVECOLUMN** содержит входные и выходные параметры для [жетретриевеколумнс](./jetretrievecolumns-function.md). Поля в структуре описывают извлекаемое значение столбца, способ его извлечения и место сохранения результатов.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Элементы

**columnid**

Идентификатор столбца для извлекаемого столбца.

**пвдата**

Указатель для начала хранения данных, извлекаемых из значения столбца.

**cbData**

Размер выделения, начиная с **пвдата**, в байтах. Операция получения столбца не будет хранить больше данных в **пвдата** , чем **cbData**.

**кбактуал**

Размер данных в байтах, получаемый операцией извлечения столбца.

**грбит**

Группа битов, содержащая параметры для извлечения столбца, которые содержат ноль или более следующих значений.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Извлекает измененное значение вместо исходного значения. Если значение не было изменено, то извлекается исходное значение. Таким образом, значение, которое еще не было вставлено или Обновлено, может быть извлечено при вставке или обновлении записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Возвращает значения столбцов из индекса без доступа к записи, если это возможно. Таким образом, необязательная Загрузка записей может быть продолжена, если нужные данные будут доступны из самих записей индекса. В случаях, когда исходное значение столбца не может быть получено из индекса из-за необратимых преобразований или усечения данных, доступ к записи будет осуществляться, а данные будут извлечены как обычные. Это параметр производительности, и его следует указывать только в том случае, если вероятно, что значение столбца может быть извлечено из индекса. Этот параметр не следует указывать, если текущим индексом является кластеризованный индекс, поскольку записи индекса для кластеризованного или первичного индекса являются записями. Этот бит не может быть установлен, если также задано JET_bitRetrieveFromPrimaryBookmark.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Извлекает значения столбцов из закладки индекса и может отличаться от значения индекса, если столбец отображается как в первичном, так и в текущем индексе. Этот параметр не следует указывать, если текущий индекс является кластеризованным или первичным индексом. Этот бит не может быть установлен, если также задано JET_bitRetrieveFromIndex.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Извлекает порядковый номер значения столбца с несколькими значениями в претинфо- &gt; итагсекуенце. В поле Итагсекуенце часто используются входные данные для получения значений столбцов с несколькими значениями из записи. Однако при извлечении значений из индекса также можно связать запись индекса с определенным порядковым номером и получить также этот порядковый номер. Получение порядкового номера может быть дорогостоящей операцией, и ее следует выполнять только при необходимости.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ Битретриевенулл</p></td>
<td><p>Извлекает значения NULL для столбцов с несколькими значениями. Если этот параметр не указан, значения NULL в столбцах с несколькими значениями будут пропускаться автоматически.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Приводит к возвращению значения NULL, если запрошенный порядковый номер равен 1, а значения для столбца в записи отсутствуют. Этот параметр влияет только на столбцы с несколькими значениями.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Этот флаг предназначен только для внутреннего использования и не предназначен для использования в приложении.</p></td>
</tr>
</tbody>
</table>


**иблонгвалуе**

Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md) или [JET_coltypLongText](./jet-coltyp.md).

**итагсекуенце**

Порядковый номер значений, содержащихся в столбце с несколькими значениями. **итагсекуенце** здесь в **JET_RETRIEVECOLUMN** может быть 0. Если значение **итагсекуенце** равно 0, то вместо данных столбца возвращается число экземпляров многозначного столбца. Значение **итагсекуенце** , равное 0, не может использоваться в вызовах [жетретриевеколумн](./jetretrievecolumn-function.md).

**колумниднексттагжед**

Значение **columnid** столбца с тегом, многозначным или разреженным столбцом, когда все столбцы с тегами извлекаются путем передачи 0 в качестве значения **columnid** в [жетретриевеколумн](./jetretrievecolumn-function.md).

**Err**

Коды ошибок и предупреждения, возвращаемые при извлечении столбца.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетретриевеколумнс](./jetretrievecolumns-function.md)

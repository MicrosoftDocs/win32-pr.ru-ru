---
description: 'Дополнительные сведения: структура JET_SETCOLUMN'
title: Структура JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809040"
---
# <a name="jet_setcolumn-structure"></a>Структура JET_SETCOLUMN


_**Применимо к:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>Структура JET_SETCOLUMN

Структура **JET_SETCOLUMN** содержит входные и выходные параметры для [жетсетколумнс](./jetsetcolumns-function.md). Поля в структуре описывают, какое значение столбца следует задать, как задать его и где можно получить данные набора столбцов.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Элементы

**columnid**

Идентификатор столбца для устанавливаемого столбца.

**пвдата**

Указатель на данные, которые необходимо задать в столбце.

**cbData**

Размер выделения в байтах, начиная с **пвдата** в байтах.

**грбит**

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Добавляет данные в столбец типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Аналогичное поведение можно добиться, определив размер существующего длинного значения и указав <strong>иблонгвалуе</strong> в <strong>псетинфо</strong>. Однако проще использовать этот <em>грбит</em>, так как знание размера существующего значения столбца не требуется.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Заменяет существующее длинное значение новыми данными. При использовании этого параметра, как будто существующее длинное значение было установлено равным 0 (нулю), перед установкой новых данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Интерпретирует входной буфер как целое число байтов, чтобы задать в качестве длины длинного значения, описываемого значением columnid, и если оно предоставлено, порядковый номер в псетинфо- &gt; итагсекуенце. Если указанный размер больше значения существующего столбца, столбец будет расширен с помощью нулей. Если размер меньше значения существующего столбца, то значение будет обрезано.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Задает нулевую длину значения. Как правило, значение столбца устанавливается равным NULL путем передачи Кбмакс 0. Однако для некоторых типов, например <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, значение столбца может быть равно 0, а не NULL, и этот параметр используется для РАЗЛИЧЕНИЯ значений NULL и нулевой длины.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Принудительное хранение длинных значений, столбцов типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, которые хранятся отдельно от оставшейся части данных записи. Обычно это происходит, когда размер длинного значения предотвращает сохранение его с помощью оставшихся данных записи. Однако этот параметр можно использовать для принудительного сохранения длинного значения. Обратите внимание, что значения типа Long, равные четырем байтам, не могут быть принудительно отделены. В таких случаях параметр игнорируется.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Применяет уникальные значения в столбце с несколькими значениями. Этот параметр сравнивает данные исходного столбца без преобразований с другими существующими значениями столбцов, и при обнаружении дубликата возвращается ошибка. Если этот параметр задан, также нельзя указывать JET_bitSetAppendLv, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Применяет уникальные значения в столбце с несколькими значениями. Этот параметр сравнивает ключевое нормализованное преобразование данных столбца с другими аналогичными преобразованными значениями столбцов, и при обнаружении дубликата возвращается ошибка. Если этот параметр задан, также нельзя указывать JET_bitSetAppendLv, JET_bitSetOverwriteLV и JET_bitSetSizeLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Приводит к тому, что столбец возвращает значение столбца по умолчанию при последующих операциях получения столбца. Все существующие значения столбцов удаляются. Этот параметр применим только к столбцам с тегами, разреженным или многозначным.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Сохраняет значение Long, столбцы типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или JET_coltypeLongBinary, сохраняя при возможности оставшиеся данные записи. Обычно длинные столбцы хранятся отдельно, если их длина превышает 1024 байт или в противном случае длина записи превысит ограничение размера страницы. Однако если этот параметр задан, операция задания столбца завершится с ошибкой JET_errColumnTooBig вместо того, чтобы хранить значение этого столбца отдельно от оставшихся данных записи.</p></td>
</tr>
</tbody>
</table>


**иблонгвалуе**

Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md)или [JET_coltypLongText](./jet-coltyp.md).

**итагсекуенце**

Описывает порядковый номер значения в столбце с несколькими значениями. Значение **итагсекуенце** , равное 0, указывает, что набор значений столбца должен быть добавлен в качестве нового экземпляра многозначного столбца.

**Err**

Коды ошибок и предупреждения, возвращаемые операцией Set Column.

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
[жетсетколумнс](./jetsetcolumns-function.md)

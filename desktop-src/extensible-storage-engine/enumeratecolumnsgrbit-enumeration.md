---
description: Дополнительные сведения о перечислении Енумератеколумнсгрбит
title: Перечисление Енумератеколумнсгрбит
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713003"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Перечисление Енумератеколумнсгрбит

Параметры для Жетенумератеколумнс.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Члены

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>енумератекомпрессаутпут</td>
<td>При перечислении значений столбцов все столбцы, для которых мы получаем все значения и которые имеют только одно значение столбца, отличного от NULL, могут быть возвращены в сжатом формате. Для таких столбцов будет задано значение <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a> , а размер значения столбца и объем памяти, содержащий значение столбца, будут возвращаться непосредственно в структуре <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . Не гарантируется, что все подходящие столбцы сжимаются таким образом. Дополнительные сведения см. в разделе <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</td>
</tr>
<tr class="odd">
<td></td>
<td>енумератекопи</td>
<td>Этот параметр указывает, что необходимо перечислить измененные значения столбца записи, а не исходные значения столбца. Если значение столбца не было изменено, исходное значение столбца перечисляется. Таким образом, значение столбца, которое еще не было вставлено или Обновлено, может быть перечислено при вставке или обновлении записи.
<p>Этот параметр идентичен <a href="hh578120(v=exchg.10).md">ретриевекопи</a>.</p></td>
</tr>
<tr class="even">
<td></td>
<td>енумератеигноредефаулт</td>
<td>Если данный столбец отсутствует в записи, значение столбца не будет возвращено. Обычно в этом случае возвращается значение по умолчанию для столбца, если таковое имеется. Гарантируется, что если в столбце задано значение, отличное от значения по умолчанию, то будет возвращено другое значение (т. е. Если для столбца со значением по умолчанию явно задано значение NULL, то в качестве значения для этого столбца будет возвращено значение NULL). Даже при запросе этого параметра по-прежнему можно увидеть значение столбца, которое должно быть равно значению по умолчанию. Для удаления значений столбцов, соответствующих значениям по умолчанию, никаких усилий не предпринимается. Важно помнить, что этот параметр влияет на выходные данные <a href="dn292148(v=exchg.10).md">жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)</a> при использовании с Енумератепресенцеонли или енумератетагжедонли.</td>
</tr>
<tr class="odd">
<td></td>
<td>енумератепресенцеонли</td>
<td>Если для запрошенного столбца или значения столбца существует значение, отличное от NULL, связанные данные не возвращаются. Вместо этого для этого столбца или значения столбца будет задано значение <a href="hh557250(v=exchg.10).md">колумнпресент</a>. Если значение столбца или столбца равно NULL, <a href="hh557250(v=exchg.10).md">колумннулл</a> будет возвращен как обычно.</td>
</tr>
<tr class="even">
<td></td>
<td>енумератетагжедонли</td>
<td>При перечислении всех значений столбцов в записи (например, если Нумколумнидс равен нулю) будут возвращены только значения столбцов с тегами. Этот параметр не допускается при перечислении определенного массива идентификаторов столбцов.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[енумератеигнореусердефинеддефаулт](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[енумератеинрекордонли](./windows7grbits.enumerateinrecordonly-field.md)

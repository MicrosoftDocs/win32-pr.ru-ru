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
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466811"
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


|  | Имя участника | Описание | 
|--|-------------|-------------|
|  | None | Параметры по умолчанию. | 
|  | енумератекомпрессаутпут | При перечислении значений столбцов все столбцы, для которых мы получаем все значения и которые имеют только одно значение столбца, отличного от NULL, могут быть возвращены в сжатом формате. Для таких столбцов будет задано значение <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a> , а размер значения столбца и объем памяти, содержащий значение столбца, будут возвращаться непосредственно в структуре <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . Не гарантируется, что все подходящие столбцы сжимаются таким образом. Дополнительные сведения см. в разделе <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . | 
|  | енумератекопи | Этот параметр указывает, что необходимо перечислить измененные значения столбца записи, а не исходные значения столбца. Если значение столбца не было изменено, исходное значение столбца перечисляется. Таким образом, значение столбца, которое еще не было вставлено или Обновлено, может быть перечислено при вставке или обновлении записи.<p>Этот параметр идентичен <a href="hh578120(v=exchg.10).md">ретриевекопи</a>.</p> | 
|  | енумератеигноредефаулт | Если данный столбец отсутствует в записи, значение столбца не будет возвращено. Обычно в этом случае возвращается значение по умолчанию для столбца, если таковое имеется. Гарантируется, что если в столбце задано значение, отличное от значения по умолчанию, то будет возвращено другое значение (т. е. Если для столбца со значением по умолчанию явно задано значение NULL, то в качестве значения для этого столбца будет возвращено значение NULL). Даже при запросе этого параметра по-прежнему можно увидеть значение столбца, которое должно быть равно значению по умолчанию. Для удаления значений столбцов, соответствующих значениям по умолчанию, никаких усилий не предпринимается. Важно помнить, что этот параметр влияет на выходные данные <a href="dn292148(v=exchg.10).md">жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)</a> при использовании с Енумератепресенцеонли или енумератетагжедонли. | 
|  | енумератепресенцеонли | Если для запрошенного столбца или значения столбца существует значение, отличное от NULL, связанные данные не возвращаются. Вместо этого для этого столбца или значения столбца будет задано значение <a href="hh557250(v=exchg.10).md">колумнпресент</a>. Если значение столбца или столбца равно NULL, <a href="hh557250(v=exchg.10).md">колумннулл</a> будет возвращен как обычно. | 
|  | енумератетагжедонли | При перечислении всех значений столбцов в записи (например, если Нумколумнидс равен нулю) будут возвращены только значения столбцов с тегами. Этот параметр не допускается при перечислении определенного массива идентификаторов столбцов. | 



## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[енумератеигнореусердефинеддефаулт](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[енумератеинрекордонли](./windows7grbits.enumerateinrecordonly-field.md)

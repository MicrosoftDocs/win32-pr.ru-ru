---
description: Дополнительные сведения о перечислении Макекэйгрбит
title: Перечисление Макекэйгрбит
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144215"
---
# <a name="makekeygrbit-enumeration"></a>Перечисление Макекэйгрбит

Параметры для Жетмакекэй.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a>Члены

<table>
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
<td>невкэй</td>
<td>Должен быть создан новый ключ поиска. Любой ранее существующий ключ поиска отклоняется.</td>
</tr>
<tr class="odd">
<td></td>
<td>нормализедкэй</td>
<td>Если указан этот параметр, все остальные параметры игнорируются, любой ранее существующий ключ поиска отбрасывается, а содержимое входного буфера загружается в качестве нового ключа поиска.</td>
</tr>
<tr class="even">
<td></td>
<td>кэйдатазероленгс</td>
<td>Если размер входного буфера равен нулю, а текущий ключевой столбец является столбцом переменной длины, этот параметр указывает, что входной буфер содержит значение нулевой длины. В противном случае размер входного буфера, равный нулю, будет означать значение NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>стрлимит</td>
<td>Этот параметр указывает, что ключ поиска должен быть создан таким, чтобы все ключевые столбцы, поступающие после текущего ключевого столбца, считались подстановочными знаками.</td>
</tr>
<tr class="even">
<td></td>
<td>субстрлимит</td>
<td>Этот параметр указывает, что ключ поиска должен быть создан таким, что текущий ключевой столбец считается подстановочным знаком, а все ключевые столбцы, поступающие после текущего ключевого столбца, должны считаться подстановочными знаками.</td>
</tr>
<tr class="odd">
<td></td>
<td>фуллколумнстартлимит</td>
<td>Ключ поиска должен быть создан таким, чтобы все ключевые столбцы, поступающие после текущего ключевого столбца, считались подстановочными знаками.</td>
</tr>
<tr class="even">
<td></td>
<td>фуллколумнендлимит</td>
<td>Ключ поиска должен быть создан таким образом, чтобы все ключевые столбцы, поступающие после текущего ключевого столбца, считались подстановочными знаками.</td>
</tr>
<tr class="odd">
<td></td>
<td>партиалколумнстартлимит</td>
<td>Ключ поиска должен быть создан таким, что текущий ключевой столбец считается подстановочным знаком, а все ключевые столбцы, поступающие после текущего ключевого столбца, должны рассматриваться как подстановочные знаки.</td>
</tr>
<tr class="even">
<td></td>
<td>партиалколумнендлимит</td>
<td>Ключ поиска должен быть создан таким, что текущий ключевой столбец считается подстановочным знаком, а все ключевые столбцы, поступающие после текущего ключевого столбца, должны рассматриваться как подстановочные знаки.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

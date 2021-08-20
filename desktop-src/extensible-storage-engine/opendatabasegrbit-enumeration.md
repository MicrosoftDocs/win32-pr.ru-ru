---
description: Дополнительные сведения о перечислении Опендатабасегрбит
title: Перечисление Опендатабасегрбит
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2bfd131d448157b44e861de4d8c167a074a3c1cefb361c3dffe085793f40c224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890756"
---
# <a name="opendatabasegrbit-enumeration"></a>Перечисление Опендатабасегрбит

Параметры для [жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)](./api.jetopendatabase-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
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
<td>ReadOnly</td>
<td>Предотвращает изменения в базе данных.</td>
</tr>
<tr class="odd">
<td></td>
<td>Монопольная блокировка</td>
<td>Разрешает присоединение базы данных только одному сеансу. Как правило, база данных может быть открыта несколькими сеансами.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: Дополнительные сведения о перечислении Жетлоккгрбит
title: Перечисление Жетлоккгрбит
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991434"
---
# <a name="getlockgrbit-enumeration"></a>Перечисление Жетлоккгрбит

Параметры для Жетжетлокк.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
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
<td>Чтение</td>
<td>Получение блокировки чтения для текущей записи. Блокировки чтения несовместимы с блокировками записи, уже удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми другими сеансами.</td>
</tr>
<tr class="even">
<td></td>
<td>запись</td>
<td>Получение блокировки записи для текущей записи. Блокировки записи несовместимы с блокировками записи или чтения, удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми в одном сеансе.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

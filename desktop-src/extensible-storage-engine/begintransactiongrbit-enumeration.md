---
description: Дополнительные сведения о перечислении Бегинтрансактионгрбит
title: Перечисление Бегинтрансактионгрбит
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8bbbba69a6768f37e816030f63aa00e5ed05f2133b62f1047b0c7cbe58d55ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982844"
---
# <a name="begintransactiongrbit-enumeration"></a>Перечисление Бегинтрансактионгрбит

Параметры для [JetBeginTransaction2 (JET_SESID, бегинтрансактионгрбит)](./api.jetbegintransaction2-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
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
<td>Транзакция не изменит базу данных. При попытке обновления эта операция завершится ошибкой с параметром <a href="hh564840(v=exchg.10).md">ReadOnly</a>. Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

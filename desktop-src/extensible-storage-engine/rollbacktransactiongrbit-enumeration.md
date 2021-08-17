---
description: Дополнительные сведения о перечислении Роллбакктрансактионгрбит
title: Перечисление Роллбакктрансактионгрбит
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b293fc938a0870b9b6db993773c311198a1c2b04566eee1e8dc5fadf72fc59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703089"
---
# <a name="rollbacktransactiongrbit-enumeration"></a>Перечисление Роллбакктрансактионгрбит

Параметры для Жетроллбакктрансактион.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
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
<td>роллбаккалл</td>
<td>Этот параметр запрашивает отмену всех изменений, внесенных в состояние базы данных во время всех точек сохранения. В результате сеанс выполнит выход из транзакции.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

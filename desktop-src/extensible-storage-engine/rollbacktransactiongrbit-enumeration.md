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
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683580"
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

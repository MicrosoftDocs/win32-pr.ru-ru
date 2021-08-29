---
description: 'Дополнительные сведения: оператор JET_COMMIT_ID. GreaterThan'
title: Оператор JET_COMMIT_ID. GreaterThan (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 55104406
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c81a9c9e3ad604e88df6c040bdc00611e4ba85b51931a1f4fded0d02e7615e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834144"
---
# <a name="jet_commit_idgreaterthan-operator"></a>JET_COMMIT_ID. GreaterThan, оператор

Определите, находится ли один коммитид перед другой коммитид.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>Параметры

  - LHS  
    Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Первый коммитид для сравнения.

<!-- end list -->

  - rhs  
    Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Второй коммитид для сравнения.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если LHS поступает после RHS.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_COMMIT_ID](./jet-commit-id-class.md)

[Элементы JET_COMMIT_ID](./jet-commit-id-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)

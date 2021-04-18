---
description: 'Дополнительные сведения о: JET_BKLOGTIME. Оператор равенства'
title: JET_BKLOGTIME. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5a75a1fc55159fc5ea71dba09dc1ed54194b940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693788"
---
# <a name="jet_bklogtimeequality-operator"></a>JET_BKLOGTIME. Оператор равенства

Определяет, равны ли два указанных экземпляра JET_BKLOGTIME.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a>Параметры

  - LHS  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Первый экземпляр для сравнения.

<!-- end list -->

  - rhs  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Второй экземпляр для сравнения.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Элементы JET_BKLOGTIME](./jet-bklogtime-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

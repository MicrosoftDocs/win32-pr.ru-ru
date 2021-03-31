---
description: 'Дополнительные сведения о: JET_INSTANCE. Оператор неравенства'
title: JET_INSTANCE. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d537b01d3485e7f5e2d1d629c005a228eac92306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156899"
---
# <a name="jet_instanceinequality-operator"></a>JET_INSTANCE. Оператор неравенства

Определяет, являются ли два указанных экземпляра JET_INSTANCE неравными.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a>Параметры

  - LHS  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Первый экземпляр для сравнения.

<!-- end list -->

  - rhs  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Второй экземпляр для сравнения.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра не равны.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_INSTANCE](./jet-instance-structure.md)

[Элементы JET_INSTANCE](./jet-instance-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

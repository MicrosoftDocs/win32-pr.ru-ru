---
description: 'Дополнительные сведения о: JET_LGPOS. Оператор неравенства'
title: JET_LGPOS. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e324131591f1d6bee3c00e6260f31f6580ec086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999058"
---
# <a name="jet_lgposinequality-operator"></a>JET_LGPOS. Оператор неравенства

Определяет, являются ли два указанных экземпляра JET_LGPOS неравными.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Параметры

  - LHS  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Первый экземпляр для сравнения.

<!-- end list -->

  - rhs  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Второй экземпляр для сравнения.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра не равны.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_LGPOS](./jet-lgpos-structure2.md)

[Элементы JET_LGPOS](./jet-lgpos-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

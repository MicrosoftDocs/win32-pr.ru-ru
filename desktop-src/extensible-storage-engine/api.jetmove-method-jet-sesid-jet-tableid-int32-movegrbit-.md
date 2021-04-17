---
description: 'Дополнительные сведения: метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)'
title: Метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100765
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6d77914a3dc4728626db8e4ffe271851099e5e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712927"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-int32-movegrbit"></a>Метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)

Навигация по индексу. Курсор может располагаться в начале или в конце индекса и перемещаться назад и вперед по заданному числу записей индекса. См. также [тримовефирст (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [тримовеласт (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [тримовенекст (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [тримовепревиаус (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As Integer, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As Integer
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, используемый для вызова.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор для позиции.

<!-- end list -->

  - нумровс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Смещение, которое указывает, насколько далеко переместить курсор.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. мовегрбит](./movegrbit-enumeration.md)  
    
    Параметры перемещения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жетмове](./api.jetmove-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

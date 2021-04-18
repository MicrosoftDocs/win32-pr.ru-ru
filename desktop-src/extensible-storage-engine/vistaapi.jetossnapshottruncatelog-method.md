---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшоттрункателог'
title: Вистаапи. Жетосснапшоттрункателог, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682380"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a>Вистаапи. Жетосснапшоттрункателог, метод

Включает усечение журнала для всех экземпляров, которые являются частью сеанса моментальных снимков.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - snapshot  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Идентификатор моментального снимка.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшоттрункателоггрбит](./snapshottruncateloggrbit-enumeration.md)  
    
    Параметры для этого вызова.

## <a name="remarks"></a>Комментарии

Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра [континуеафтерсав](./vistagrbits.continueafterthaw-field.md) . В противном случае сеанс моментального снимка заканчивается после вызова [жетосснапшотсав (JET_OSSNAPID, снапшотсавгрбит)](./api.jetossnapshotthaw-method.md).

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Вистаапи](./vistaapi-class.md)

[Элементы Вистаапи](./vistaapi-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшоттрункателогинстанце'
title: Вистаапи. Жетосснапшоттрункателогинстанце, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913747"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>Вистаапи. Жетосснапшоттрункателогинстанце, метод

Усекает журнал для указанного экземпляра во время сеанса моментального снимка.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - snapshot  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Идентификатор моментального снимка.

<!-- end list -->

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр, для которого необходимо усечь журнал.

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

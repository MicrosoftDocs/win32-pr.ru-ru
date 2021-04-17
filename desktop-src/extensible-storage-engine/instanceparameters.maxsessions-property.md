---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макссессионс'
title: Инстанцепараметерс. Макссессионс, свойство
TOCTitle: 'MaxSessions property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxsessions(v=EXCHG.10)
ms:contentKeyID: 55103557
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxSessions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2294a8de2e3603a638607efad5baaa6af6c1ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712593"
---
# <a name="instanceparametersmaxsessions-property"></a>Инстанцепараметерс. Макссессионс, свойство

Возвращает или задает количество ресурсов сеансов, зарезервированных для данного экземпляра. Ресурс сеанса непосредственно соответствует JET_SESID.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property MaxSessions As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxSessions

instance.MaxSessions = value
```

``` csharp
public int MaxSessions { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

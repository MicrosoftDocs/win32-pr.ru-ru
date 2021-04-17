---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Версионсторетасккуеуемакс'
title: Инстанцепараметерс. Версионсторетасккуеуемакс, свойство
TOCTitle: 'VersionStoreTaskQueueMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.versionstoretaskqueuemax(v=EXCHG.10)
ms:contentKeyID: 55103554
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_VersionStoreTaskQueueMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd522fa46df40182b6dfe638e7663df8e9e56c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498153"
---
# <a name="instanceparametersversionstoretaskqueuemax-property"></a>Инстанцепараметерс. Версионсторетасккуеуемакс, свойство

Возвращает или задает количество рабочих элементов фоновой очистки, которые могут быть поставлены в очередь пула потоков компонента Database Engine в любой момент времени.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property VersionStoreTaskQueueMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.VersionStoreTaskQueueMax

instance.VersionStoreTaskQueueMax = value
```

``` csharp
public int VersionStoreTaskQueueMax { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Максверпажес'
title: Инстанцепараметерс. Максверпажес, свойство
TOCTitle: 'MaxVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxverpages(v=EXCHG.10)
ms:contentKeyID: 55103318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxVerPages
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd6a561a4005ab0992f6d32dbe6c65a241f517d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105711999"
---
# <a name="instanceparametersmaxverpages-property"></a>Инстанцепараметерс. Максверпажес, свойство

Возвращает или задает максимальное число страниц хранилища версий, зарезервированных для данного экземпляра.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property MaxVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxVerPages

instance.MaxVerPages = value
```

``` csharp
public int MaxVerPages { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

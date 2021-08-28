---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макскурсорс'
title: Инстанцепараметерс. Макскурсорс, свойство
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08418b7f15c538c20e04ce4ce42c2bb2996f37f31c7198ff8ba840c21268f5c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116364"
---
# <a name="instanceparametersmaxcursors-property"></a>Инстанцепараметерс. Макскурсорс, свойство

Возвращает или задает количество ресурсов курсора, зарезервированных для данного экземпляра. Ресурс курсора непосредственно соответствует JET_TABLEID.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

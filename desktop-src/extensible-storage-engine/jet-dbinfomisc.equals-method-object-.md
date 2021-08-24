---
description: 'Дополнительные сведения о: JET_DBINFOMISC. Метод Equals (Object)'
title: JET_DBINFOMISC. Метод Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39513216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46be2130cbb57cc216f570e944d6959ae355780134f90bc94101d01d6f38bb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617604"
---
# <a name="jet_dbinfomiscequals-method-object"></a>JET_DBINFOMISC. Метод Equals (Object)

Определяет, равен ли указанный [объект](/dotnet/api/system.object) текущему [объекту](/dotnet/api/system.object).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Параметры

  - obj  
    Тип: [System. Object](/dotnet/api/system.object)  
    
    [Объект](/dotnet/api/system.object) , сравниваемый с текущим [объектом](/dotnet/api/system.object).

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если указанный [объект](/dotnet/api/system.object) равен текущему [объекту](/dotnet/api/system.object); в противном случае — значение false.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Элементы JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Перегрузка Equals](./jet-dbinfomisc.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

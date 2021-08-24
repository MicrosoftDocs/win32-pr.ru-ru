---
description: 'Дополнительные сведения о: JET_INSTANCE_INFO. Метод Equals (Object)'
title: JET_INSTANCE_INFO. Метод Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103694
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a067043df54722a86f2385043d96cc0ce590653eda437c8379536e494a2eece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473914"
---
# <a name="jet_instance_infoequals-method-object"></a>JET_INSTANCE_INFO. Метод Equals (Object)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
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
    
    Объект для сравнения с данным экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INSTANCE_INFO](./jet-instance-info-class.md)

[Элементы JET_INSTANCE_INFO](./jet-instance-info-members.md)

[Перегрузка Equals](./jet-instance-info.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

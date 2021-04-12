---
description: 'Дополнительные сведения о: JET_INSTANCE. Метод Equals (JET_INSTANCE)'
title: JET_INSTANCE. Метод Equals (JET_INSTANCE)
TOCTitle: Equals method (JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39512490
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be4f2a172da5fc0d7670e7e87464eac04df3cfa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265733"
---
# <a name="jet_instanceequals-method-jet_instance"></a>JET_INSTANCE. Метод Equals (JET_INSTANCE)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim other As JET_INSTANCE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_INSTANCE](./jet-instance-structure.md)

[Элементы JET_INSTANCE](./jet-instance-members.md)

[Перегрузка Equals](./jet-instance.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
